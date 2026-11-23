---
id: use-case/build-an-agent
type: use-case
slug: build-an-agent
schema_version: 3.0
title: Build an Agent
label: Build an agent
order: 2
goal: Let a language model plan its own steps, call tools, read their results and loop until a multi-step task is done, inside limits you set.
stages:
- id: loop
  name: Agent loop
  note: Runs on every step the agent takes.
- id: tools
  name: Tools and environment
  note: Runs whenever the agent acts on the outside world.
- id: safety
  name: Safety
  note: Runs before a tool call executes and on everything that enters the context.
- id: quality
  name: Quality and operations
  note: Runs before each release and continuously in production.
blocks:
- id: orchestration
  stage: loop
  name: Agent framework
  purpose: Runs the loop of model call, tool call and result, and holds the state, branching and handoffs between agents.
  options:
  - record: framework/langgraph
    choice: default
    when: MIT-licensed low-level orchestration for long-running, stateful agents, with durable execution, human-in-the-loop review and short- and long-term memory, usable without LangChain.
  - record: framework/openai-agents-python
    choice: alternative
    when: Pick it for a small set of primitives (agents, handoffs, guardrails, sessions, tracing) that is provider-agnostic and MIT-licensed.
  - record: framework/google-adk
    choice: alternative
    when: Pick it for multi-agent hierarchies with a development UI and evaluation; it is optimised for Gemini but model-agnostic, under Apache-2.0.
  - record: framework/claude-agent-sdk
    choice: alternative
    when: Pick it to embed the Claude Code agent loop, built-in file, shell and web tools, permissions, hooks and subagents in a Python or TypeScript app.
  - record: framework/mastra
    choice: alternative
    when: Pick it for a TypeScript stack; it combines agents, graph-based workflows, memory, evals and observability, with its core under Apache-2.0.
  how_to_choose:
  - Start with predefined workflows; let the model direct its own steps only where the task needs it.
  - 'Need pause, resume and human review on long runs: pick a framework with durable state.'
  - 'Writing TypeScript: Mastra or the Claude Agent SDK, which ships Python and TypeScript.'
  browse:
    label: All agent frameworks
    record: framework-category/agents
- id: model
  stage: loop
  name: Tool-calling model
  purpose: Decides the next step, chooses which tool to call with which arguments, and writes the final answer.
  options:
  - record: model/gpt-oss-20b
    choice: default
    when: Apache-2.0 open weights trained for function calling with defined schemas, browsing and code execution, with configurable reasoning effort.
  - record: model/qwen3-8b
    choice: alternative
    when: Pick it for Apache-2.0 weights with tool calling, more than a hundred languages, and a per-request switch between thinking and non-thinking modes.
  how_to_choose:
  - Shortlist on the tool-use benchmarks below, then test on your own tools.
  - gpt-oss works correctly only with the harmony response format; serve it through a runtime its model card names.
  browse:
    label: All tool-calling models
    record: task/tool-calling-models
- id: model-access
  stage: loop
  name: Model access
  purpose: Gives the agent one API to reach hosted or self-served models, with retries and fallbacks between them.
  options:
  - record: framework/litellm
    choice: default
    when: Calls many model providers in the OpenAI format, as a Python library or a self-hosted gateway with virtual keys, spend tracking, load balancing and fallbacks.
  - record: framework/vllm
    choice: alternative
    when: Pick it to self-serve open-weight models behind an OpenAI-compatible server on GPUs.
  - record: framework/ollama
    choice: alternative
    when: Pick it to run open models on a developer machine behind a REST API.
  how_to_choose:
  - Use a gateway when the agent must switch providers or fall back on failure.
  - Self-serve when data must not leave your infrastructure.
- id: memory
  stage: loop
  name: Long-term memory
  purpose: Keeps facts about users and past sessions outside the context window and returns the relevant ones on later runs.
  options:
  - record: framework/mem0
    choice: default
    when: Apache-2.0 memory layer that keeps user, session and agent state, available as a library, a self-hosted server or a hosted platform.
  - record: framework/graphiti
    choice: alternative
    when: Pick it when facts change over time; it builds a temporal context graph that marks superseded facts invalid instead of deleting them.
  how_to_choose:
  - Use the framework's own conversation state for a single session; add a memory layer only for recall across sessions.
  - 'Facts that change and need history: a temporal graph; preferences and profile facts: a memory layer.'
- id: tool-protocol
  stage: tools
  name: Tool interface
  purpose: Exposes your functions, data and APIs to the agent with typed schemas it can call.
  options:
  - record: framework/python-sdk
    choice: default
    when: The official Python implementation of the Model Context Protocol (MCP), the open standard for connecting AI applications to tools and data, for both servers and clients.
  - record: framework/fastmcp
    choice: alternative
    when: Pick it for a higher-level Python framework that generates tool schemas and validation from functions; its first version was folded into the official SDK.
  - record: framework/composio
    choice: alternative
    when: Pick it for ready-made, pre-authenticated toolkits for many apps, scoped per user and exposed over a hosted MCP endpoint.
  how_to_choose:
  - Write tools as MCP servers so any MCP-capable framework can use them.
  - Use hosted integrations when per-user authentication to third-party apps is the hard part.
  browse:
    label: All agent tools
    record: framework-category/agents
- id: web-actions
  stage: tools
  name: Browser actions
  purpose: Lets the agent read pages and act in a real browser when no API exists.
  options:
  - record: framework/browser-use
    choice: default
    when: MIT-licensed Python library that gives a model a real browser, works with many model providers, and runs locally or on a hosted browser.
  - record: framework/stagehand
    choice: alternative
    when: Pick it to mix code with natural-language act, observe and extract steps that return schema-validated data, in TypeScript, Python or Go.
  how_to_choose:
  - Prefer an API or an MCP tool when one exists; browsers are slower and break when pages change.
  - 'Need deterministic steps with a few model-driven ones: Stagehand.'
- id: code-sandbox
  stage: tools
  name: Code execution sandbox
  purpose: Runs code the agent writes in an isolated environment so it cannot touch the host or your data.
  options:
  - record: framework/e2b
    choice: default
    when: Apache-2.0 infrastructure that runs AI-generated code in isolated cloud sandboxes through Python and JavaScript SDKs, and can be self-hosted.
  - name: gVisor
    url: https://gvisor.dev/docs/
    choice: alternative
    when: Pick it to harden your own containers; it is an application kernel with an OCI runtime that plugs into Docker and Kubernetes.
  how_to_choose:
  - Never run model-written code in the agent's own process or on a host with credentials.
  - 'Need managed sandboxes: E2B; run your own container platform: gVisor.'
- id: tool-approval
  stage: safety
  name: Tool permissions and approval
  purpose: Decides which tool calls run automatically and which wait for a person, and limits each tool to what the task needs.
  options:
  - record: framework/langgraph
    choice: default
    when: Its human-in-the-loop support lets a person review and change the agent's state at any point in a run, so a tool call can wait for approval.
  - record: framework/claude-agent-sdk
    choice: alternative
    when: Pick it for permission settings that control which tools run automatically and which need approval, plus hooks at points in the agent lifecycle.
  - record: framework/google-adk
    choice: alternative
    when: Pick it to guard tool execution with explicit confirmation and custom input.
  - record: framework/openai-agents-python
    choice: alternative
    when: Pick it for built-in human-in-the-loop mechanisms across agent runs.
  how_to_choose:
  - Grant each tool the least privilege its task requires.
  - Require human approval for privileged or irreversible operations.
  - Use the approval mechanism of the framework that already runs your loop.
- id: injection-defence
  stage: safety
  name: Prompt-injection defence
  purpose: Screens user input and tool results for instructions that try to take over the agent, and checks tool calls before they run.
  options:
  - record: framework/nemo-guardrails
    choice: default
    when: Apache-2.0 library with input, output, tool-call and tool-result rails, so checks run before a tool executes and on what it returns, independent of the agent framework.
  - record: model/llama-prompt-guard-2-86m
    choice: alternative
    when: Pick it to classify untrusted text (web pages, files, tool output) as benign or malicious for prompt injection and jailbreaks; it is multilingual.
  - record: model/llama-guard-4-12b
    choice: alternative
    when: Pick it to classify prompts and responses for safety hazards, including a code-interpreter-abuse category.
  how_to_choose:
  - Treat every tool result as untrusted; indirect injection arrives through web pages and files.
  - Mark untrusted content apart from instructions in the prompt.
  - A classifier lowers risk but does not remove it; keep sandboxing and approval in place.
  browse:
    label: All guardrail and safety tools
    record: framework-category/guardrails
- id: evaluation
  stage: quality
  name: Evaluation
  purpose: Scores whether the agent completed its task and called the right tools with the right arguments, over whole trajectories.
  options:
  - record: framework/deepeval
    choice: default
    when: Apache-2.0 framework with task-completion and tool-correctness metrics that evaluates traced agent trajectories as pytest-style tests.
  - record: framework/ragas
    choice: alternative
    when: Pick it for tool-call accuracy, tool-call F1, agent goal accuracy and topic adherence metrics.
  - record: framework/promptfoo
    choice: alternative
    when: Pick it for red teaming and vulnerability scanning of the agent alongside declarative tests in CI.
  how_to_choose:
  - Evaluate the trajectory (which tools, in what order), not only the final answer.
  - Run red-team tests against the tools the agent can reach.
  browse:
    label: All evaluation tools
    record: framework-category/evaluation
- id: benchmarks
  stage: quality
  name: Benchmarks for model choice
  purpose: Compares candidate models on public tool-use and safety tasks before you test them on your own.
  options:
  - record: benchmark/bfcl-v4
    choice: default
    when: The Berkeley Function Calling Leaderboard measures how accurately models call functions, from single calls to multi-turn and agentic tasks.
  - record: benchmark/tau2-bench
    choice: alternative
    when: Use it for agents that talk to users; it simulates customer-service conversations with domain rules, tools and a simulated user, across several domains.
  - record: benchmark/agentdojo
    choice: alternative
    when: Use it to compare how well models and defences resist prompt injection in tool-using agents.
  how_to_choose:
  - Read the benchmark closest to your task; a function-calling score says little about long conversations.
  - Check injection robustness separately from task success.
- id: tracing
  stage: quality
  name: Tracing and observability
  purpose: Records every model call, tool call and intermediate step of a run so a failed task can be replayed step by step.
  options:
  - record: framework/langfuse
    choice: default
    when: Open-source platform built on OpenTelemetry that traces agent actions and model calls, evaluates them, and can be self-hosted.
  - record: framework/langsmith
    choice: alternative
    when: Pick it for tracing and evaluation in one platform, with cloud, hybrid or self-hosted setups.
  - record: framework/mlflow
    choice: alternative
    when: Pick it when you already run MLflow; its tracing is OpenTelemetry-compatible and the data stays on your infrastructure.
  - record: framework/arize-phoenix
    choice: alternative
    when: Pick it for self-hosted OpenTelemetry tracing with evals; it is licensed under the Elastic License 2.0.
  how_to_choose:
  - Trace tool arguments and results, not only model prompts.
  - Prefer a tool that accepts OpenTelemetry so you can switch backends later.
learn_next:
- title: Building effective agents
  url: https://www.anthropic.com/engineering/building-effective-agents
  kind: blog
- title: What is the Model Context Protocol?
  url: https://modelcontextprotocol.io/docs/getting-started/intro
  kind: docs
- title: OWASP LLM01:2025 Prompt Injection
  url: https://genai.owasp.org/llmrisk/llm01-prompt-injection/
  kind: docs
- title: AgentDojo
  url: https://github.com/ethz-spylab/agentdojo
  kind: docs
related_use_cases:
- use-case/build-a-rag-app
- use-case/build-multimodal-app
- use-case/serve-in-production
- use-case/make-llm-app-safe-and-accurate
tags:
- agents
- tool-calling
- mcp
- orchestration
- prompt-injection
- llm
updated: '2026-11-21'
sources:
- url: https://www.anthropic.com/engineering/building-effective-agents
  title: Building effective agents (Anthropic)
  trust: 0.9
- url: https://github.com/langchain-ai/langgraph
  title: LangGraph repository
  trust: 0.9
- url: https://github.com/openai/openai-agents-python
  title: OpenAI Agents SDK repository
  trust: 0.9
- url: https://github.com/google/adk-python
  title: Agent Development Kit (ADK) repository
  trust: 0.9
- url: https://code.claude.com/docs/en/agent-sdk/overview
  title: Claude Agent SDK overview
  trust: 0.9
- url: https://github.com/mastra-ai/mastra
  title: Mastra repository
  trust: 0.9
- url: https://huggingface.co/openai/gpt-oss-20b
  title: openai/gpt-oss-20b model card
  trust: 0.9
- url: https://huggingface.co/Qwen/Qwen3-8B
  title: Qwen/Qwen3-8B model card
  trust: 0.9
- url: https://github.com/BerriAI/litellm
  title: LiteLLM repository
  trust: 0.9
- url: https://docs.litellm.ai/docs/simple_proxy
  title: LiteLLM AI Gateway documentation
  trust: 0.9
- url: https://github.com/vllm-project/vllm
  title: vLLM repository
  trust: 0.9
- url: https://github.com/ollama/ollama
  title: Ollama repository
  trust: 0.9
- url: https://github.com/mem0ai/mem0
  title: Mem0 repository
  trust: 0.9
- url: https://github.com/getzep/graphiti
  title: Graphiti repository
  trust: 0.9
- url: https://modelcontextprotocol.io/docs/getting-started/intro
  title: What is the Model Context Protocol (MCP)?
  trust: 0.9
- url: https://github.com/modelcontextprotocol/python-sdk
  title: MCP Python SDK repository
  trust: 0.9
- url: https://github.com/PrefectHQ/fastmcp
  title: FastMCP repository
  trust: 0.9
- url: https://github.com/ComposioHQ/composio
  title: Composio repository
  trust: 0.9
- url: https://github.com/browser-use/browser-use
  title: Browser Use repository
  trust: 0.9
- url: https://github.com/browserbase/stagehand
  title: Stagehand repository
  trust: 0.9
- url: https://github.com/e2b-dev/E2B
  title: E2B repository
  trust: 0.9
- url: https://gvisor.dev/docs/
  title: gVisor documentation
  trust: 0.9
- url: https://genai.owasp.org/llmrisk/llm01-prompt-injection/
  title: OWASP LLM01:2025 Prompt Injection
  trust: 0.9
- url: https://github.com/NVIDIA-NeMo/Guardrails
  title: NeMo Guardrails repository
  trust: 0.9
- url: https://huggingface.co/meta-llama/Llama-Prompt-Guard-2-86M
  title: meta-llama/Llama-Prompt-Guard-2-86M model card
  trust: 0.9
- url: https://huggingface.co/meta-llama/Llama-Guard-4-12B
  title: meta-llama/Llama-Guard-4-12B model card
  trust: 0.9
- url: https://github.com/confident-ai/deepeval
  title: DeepEval repository
  trust: 0.9
- url: https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/
  title: Ragas available metrics
  trust: 0.9
- url: https://github.com/promptfoo/promptfoo
  title: promptfoo repository
  trust: 0.9
- url: https://gorilla.cs.berkeley.edu/leaderboard.html
  title: Berkeley Function Calling Leaderboard
  trust: 0.9
- url: https://github.com/sierra-research/tau2-bench
  title: tau2-bench repository
  trust: 0.9
- url: https://github.com/ethz-spylab/agentdojo
  title: AgentDojo repository
  trust: 0.9
- url: https://github.com/langfuse/langfuse
  title: Langfuse repository
  trust: 0.9
- url: https://docs.langchain.com/langsmith
  title: LangSmith documentation
  trust: 0.9
- url: https://mlflow.org/docs/latest/genai/tracing/
  title: MLflow Tracing documentation
  trust: 0.9
- url: https://github.com/Arize-ai/phoenix
  title: Arize Phoenix repository
  trust: 0.9
---

## Overview

An agent is a model that directs its own steps: it reads the task, calls a tool, reads the result and repeats. The **loop** blocks pick the framework, model, model access and memory; the **tools** blocks decide what the agent can touch.

**Safety** blocks limit tool permissions, require approval for risky calls and screen untrusted content for prompt injection. **Quality** blocks evaluate whole trajectories, compare models on public benchmarks and trace every step.
