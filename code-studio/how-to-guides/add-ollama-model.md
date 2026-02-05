---
title: How to Configure Ollama Models in Code Studio
description: Instructions to configure ollama models within Syncfusion Code Studio. Use this feature to connect your preferred ollama model.
platform: syncfusion-code-studio
control: IDE
documentation: Getting Started
keywords: code, IDE, opensource, models, ollama
---




# How to Configure Ollama Models in Code Studio
 
## Overview

This guide provides step-by-step instructions to configure and use **Ollama** models inside **Code Studio**. By connecting Ollama, you can run powerful open-source language models locally on your machine. This enables private, offline-capable, and cost-free AI assistance without relying on external cloud providers or API keys.
 
## When to Use
- When you want free, unlimited usage with no API costs or rate limits – perfect for long coding sessions or agent workflows.

- When you need full privacy – your code or data must never leave your computer (sensitive projects, company policy, or offline work).
 
## Prerequisites
Before starting, ensure you have system requirement to install open-source models.

- Refer this documentation for system requirement to install Ollama
  - MacOS - [MacOS](https://docs.ollama.com/macos)
  - Windows - [Windows](https://docs.ollama.com/windows)

- Minimum hardware guidance (approximate):
  - 8–16 GB RAM for small models; 32+ GB recommended for large models.
  - GPU recommended for best performance on large models (check provider docs for GPU requirements).
 
## Download and Install steps
Refer the documentation below to download and install Ollama in your machine.
 
- [Ollama](https://docs.ollama.com/quickstart)
 
## Quick checklist before configuring
- Provider runtime installed (Ollama).

- At least one model downloaded/installed locally.

- Recommended models – deepseek-r1, qwen 2.5

- Code Studio up-to-date (latest stable release recommended).
 
## Configure Ollama Model in Code studio
- Click the model dropdown in chat box and click 'Manage Models' option.

<img src="./howtoguide-images/model_drop_down.png" alt="configure open source models">
 
- In the **Manage Language Models** dialog that appears at the top, Choose **Ollama** from the provider list

 <img src="./howtoguide-images/Provider_list.png" alt="configure open source models">

- The available locally installed models will appear in the dialogue. You can select the installed ollama model in a model list, then click ok to close the dialogue. 

<img src="./howtoguide-images/installed_model_list.png" alt="configure open source models">

- The selected Ollama model will now automatically appear in the main **model dropdown** under the **Other MOdels** section and you can start using it right away.

<img src="./howtoguide-images/model_in_drop_down.png" alt="configure open source models">