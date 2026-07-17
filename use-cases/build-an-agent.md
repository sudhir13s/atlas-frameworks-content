---
id: use-case/build-an-agent
type: use-case
slug: build-an-agent
schema_version: 1.0
title: "Build an Agent"
label: "Build an agent"
order: 2
goal: "Let an LLM plan and act — call tools, read results, and loop — to complete a multi-step task on its own."
languages: [python, typescript]
levels: [intermediate, advanced]
stack:
  - frameworkId: langchain
    role: "Agent + tool framework"
    why: "LangGraph (part of the LangChain stack) gives you a durable, inspectable graph for the reason-act loop."
    install: "pip install langgraph langchain"
    quickstartUrl: "https://langchain-ai.github.io/langgraph/tutorials/introduction/"
    docsUrl: "https://langchain-ai.github.io/langgraph/"
  - frameworkId: litellm
    role: "Model gateway"
    why: "One OpenAI-shaped interface across 100+ providers, so you can swap or fall back models without code changes."
    install: "pip install litellm"
    quickstartUrl: "https://docs.litellm.ai/docs/"
    docsUrl: "https://docs.litellm.ai/docs/"
  - frameworkId: crewai
    role: "Multi-agent orchestration"
    why: "When one agent is not enough, CrewAI structures role-based agents that collaborate on a task."
    install: "pip install crewai"
    quickstartUrl: "https://docs.crewai.com/introduction"
    docsUrl: "https://docs.crewai.com/"
  - frameworkId: langsmith
    role: "Tracing + eval"
    why: "Agents fail in the middle of a loop; LangSmith traces every step so you can see where and why."
    install: "pip install langsmith"
    quickstartUrl: "https://docs.smith.langchain.com/"
    docsUrl: "https://docs.smith.langchain.com/"
day1Plan:
  - step: 1
    task: "Define one tool well"
    estimate: "30 min"
    details: "Give it a precise name, a typed signature, and a docstring the model can read. Start with a single tool."
  - step: 2
    task: "Build the reason-act loop"
    estimate: "45 min"
    details: "Use a LangGraph ReAct agent: the model decides to call the tool, sees the result, and decides again."
  - step: 3
    task: "Add tracing"
    estimate: "20 min"
    details: "Turn on LangSmith so every model call and tool call is captured for debugging."
  - step: 4
    task: "Add a stop condition + guardrails"
    estimate: "45 min"
    details: "Cap the loop (max steps), validate tool inputs, and add a final-answer check so it cannot spin forever."
starterTemplates:
  - name: "LangGraph ReAct agent"
    repo: "https://github.com/langchain-ai/react-agent"
    why: "Official template for a tool-calling ReAct agent with tracing wired in."
  - name: "CrewAI examples"
    repo: "https://github.com/crewAIInc/crewAI-examples"
    why: "Runnable multi-agent crews to copy the role/task structure from."
learnNext:
  - title: "ReAct: Synergizing Reasoning and Acting in Language Models"
    url: "https://arxiv.org/abs/2210.03629"
    kind: paper
  - title: "LangGraph — quickstart"
    url: "https://langchain-ai.github.io/langgraph/tutorials/introduction/"
    kind: docs
  - title: "CrewAI — core concepts"
    url: "https://docs.crewai.com/concepts/agents"
    kind: docs
pitfalls:
  - "No step cap: an agent with no max-iterations budget can loop forever and burn tokens. Always bound it."
  - "Too many tools at once: the model gets confused. Add tools one at a time and test each."
  - "Trusting tool output blindly: validate and sandbox anything an agent can execute (code, shell, HTTP)."
whenToLevelUp: "When a single agent stalls on complex tasks, move to a multi-agent design (CrewAI/AutoGen) with clear roles; when reliability matters, add evals and human-in-the-loop checkpoints."
community:
  - name: "LangChain Discord"
    url: "https://www.langchain.com/join-community"
  - name: "CrewAI community"
    url: "https://community.crewai.com/"
  - name: "Latent Space"
    url: "https://www.latent.space/"
dontUse:
  - what: "An agent when a single prompt would do"
    why: "Loops add latency, cost, and failure modes. If the task is one step, just call the model once."
  - what: "Hand-rolled retry/parse loops"
    why: "A framework's structured tool-calling handles parsing and retries you would otherwise reinvent badly."
relatedUseCases: [use-case/build-a-rag-app, use-case/serve-in-production]
tags: [agents, tools, react, orchestration]
updated: 2026-07-17
sources:
  - { url: "https://langchain-ai.github.io/langgraph/", title: "LangGraph documentation", trust: 0.9 }
  - { url: "https://arxiv.org/abs/2210.03629", title: "ReAct: Synergizing Reasoning and Acting in Language Models", trust: 0.95 }
  - { url: "https://docs.crewai.com/", title: "CrewAI documentation", trust: 0.85 }
---

## Overview
An agent is an LLM in a loop with tools: it reasons about the goal, chooses a tool, reads the result,
and decides what to do next — until the task is done. The ReAct pattern (reason + act) is the template
almost every framework still follows.

## Why this stack
LangGraph gives the loop a durable, inspectable structure instead of a tangle of retries. LiteLLM lets
you swap the underlying model (or fall back on failure) without touching agent code. CrewAI is there
for when one agent is not enough and you need collaborating roles. LangSmith is non-negotiable:
agents fail mid-loop, and without tracing you are debugging blind.

## Notes
Two rules keep agents sane: bound the loop (max steps) and add tools incrementally. Guardrails are not
optional — anything the agent can execute must be validated and sandboxed. Reach for multi-agent
designs only after a single agent has clearly hit its ceiling.
