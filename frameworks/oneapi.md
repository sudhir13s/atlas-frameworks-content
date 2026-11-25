---
id: framework/oneapi
type: framework
slug: oneapi
schema_version: 3.0
title: oneAPI
status: curated
category: framework-category/gpu-programming
subcategory: compute-stack
tagline: Libraries, open-source repositories and SYCL-based C++ extensions for programming across architectures and vendors.
description: oneAPI is Intel's multi-architecture, multi-vendor programming platform, built on SYCL from The Khronos Group as a C++ extension. Intel's toolkit bundles the DPC++/C++ compiler, the DPC++ Compatibility Tool for migrating CUDA code to SYCL, and performance libraries such as oneMKL, oneDNN, oneCCL, oneDAL, oneDPL and oneTBB, plus VTune Profiler and Advisor. It targets Intel CPUs and GPUs, and NVIDIA and AMD GPUs through Codeplay plug-ins. The UXL Foundation maintains the open oneAPI specification.
best_for: Programming Intel CPUs and GPUs, and writing SYCL code portable across GPU vendors
not_ideal_for: Projects that cannot take a SYCL or Intel compiler dependency
key_features:
- DPC++/C++ compiler for SYCL
- DPC++ Compatibility Tool for migrating CUDA code to SYCL
- oneDNN deep-learning primitives and oneMKL math library
- oneCCL collective communications library
- VTune Profiler and Advisor
- NVIDIA and AMD GPU support through Codeplay plug-ins
use_cases:
- Running deep-learning workloads on Intel Arc and Data Center GPUs
- Porting CUDA code to SYCL
- High-performance computing on Intel CPUs
pros:
- Open specification maintained by the UXL Foundation, whose steering members include AMD, Arm, Google Cloud, Intel and Qualcomm
- oneDNN is used by PyTorch, TensorFlow, ONNX Runtime and OpenVINO
- Supports Linux and Windows, including WSL 2
cons:
- Toolkit components carry different licences (Intel developer-tools EULA, Intel Simplified Software License, open-source licences)
- A full installation needs about 24 GB of disk space
languages_supported:
- C++
- SYCL
- Fortran
- Python
maintained_by: Intel
license_note: Intel End User License Agreement for Developer Tools (compilers and analysis tools) and Intel Simplified Software License (performance libraries such as oneMKL); open-source components such as oneDNN (Apache-2.0) under their own licences
docs_url: https://www.intel.com/content/www/us/en/developer/tools/oneapi/overview.html
website_url: https://www.intel.com/content/www/us/en/developer/tools/oneapi/overview.html
backing:
  type: corporate
  orgs:
  - organization/intel
alternatives:
- framework/rocm
- framework/triton
ecosystem_connections:
- framework/pytorch
- framework/tensorflow
- framework/onnx-runtime
aliases:
- Intel oneAPI
- Intel oneAPI Base Toolkit
- Intel oneAPI Toolkit
tags:
- gpu-programming
- intel
- sycl
- gpu
updated: '2026-11-25'
sources:
- url: https://www.intel.com/content/www/us/en/developer/tools/oneapi/overview.html
  title: Intel oneAPI overview (Intel)
- url: https://www.intel.com/content/www/us/en/developer/articles/system-requirements/oneapi-base-toolkit/2025.html
  title: Intel oneAPI Base Toolkit system requirements (Intel)
- url: https://www.intel.com/content/www/us/en/developer/articles/license/end-user-license-agreement.html
  title: Intel End User License Agreements (Intel)
- url: https://uxlfoundation.org/
  title: UXL Foundation
- url: https://github.com/uxlfoundation/oneDNN
  title: oneDNN repository
---


