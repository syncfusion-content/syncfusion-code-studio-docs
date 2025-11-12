---
title: How to Add Local Models
Description: Steps to add local chat models in Code Studio, including adding provider API/LLM keys and registering models.
platform: syncfusion-code-studio
keywords: local,models
---

# How to add local models 

## Purpose
To enable users to configure and use their own chat models locally within the application by adding them with the appropriate API keys.

## When to Use
- When you need to access or switch between different chat models from various providers within a unified interface.
- When adding a new model to expand the capabilities or options available for AI-powered tasks. 

## Prerequisites
-The API key for the chat model provider you want to add (e.g., OpenAI, Anthropic, etc.). 

## Steps:

Click the model's section dropdown and click 'Add Chat Model' option.

<img src="../reference-images/localmodel1.png" alt="local">

In the Add Chat Model dialog box choose the provider and model you want to use and add the API key of that particular provider and click connect button.

<img src="../reference-images/localmodel2.png" alt="local">

you can see the added model appear in local model category in model's section

<img src="../reference-images/localmodel3.png" alt="local">

## Validation
- Verify that the added model appears under the local model category in the model’s section.
- Ensure the model can be selected for chat or other intended tasks.
- Perform a quick test (if possible) by issuing a simple query to the new model to confirm connectivity and functionality.

## Troubleshooting
- **Model Does Not Appear**:Ensure all fields (provider, model, API key) are filled correctly and try reconnecting.
- **Connection Fails**: Double-check that the API key is valid.