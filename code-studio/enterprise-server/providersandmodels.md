---
title: Configure LLM Providers and Models in Syncfusion Code Studio
description: Admin guide to connect LLM providers, manage API keys, and add models to your enterprise catalog in Code Studio.
platform: syncfusion-code-studio
keywords: llm, providers, models, configuration, admin, enterprise, syncfusion, code-studio, api keys, model catalog, openai, anthropic, azure openai, gemini
---

# Configure LLM Providers and Models

This guide provides step-by-step instructions for administrators to configure Large Language Model (LLM) providers and manage models within Code Studio.

> **Note**: Only admins can configure LLM providers and models.


## When to Use

- As an admin, when you need to centrally manage LLM provider credentials for your organization.
- When selecting and configuring a custom list of AI models to meet specific team or enterprise needs.
- To set default models for key AI modes like Chat, Apply, Edit, and Autocomplete.



## Prerequisites

- Admin role (check **Users & Teams**).
- Fresh API key from any LLM.

## 1. Adding an LLM Provider

To integrate an LLM provider into Code Studio:

**Steps:**

1. Navigate to the **LLM keys** page under the BYOK section. 
2. Click on **“Add LLM Key”**.  
3. In the dialog box:
   - **Provider Name**: Enter the name of the LLM provider (e.g., OpenAI, Anthropic).  
   - **API Key**: Paste the API key provided by the LLM service.  
4. Click **“Add”** to save the provider.
  <img src="./enterprise-images/llm and providers.png" alt="Provider" />

✅ Once added, the provider will be available for model selection.

## 2. Adding BYOK Models

To add a model under a configured provider:

**Steps:**

1. Go to the **Models** page under the BYOK section. 
2. Use the **search bar** to look for a specific model.  
3. Click **“Add Model”**.  
4. In the form:
   - **Provider**: Select from the list of configured providers.  
   - **Model**: Choose from the dropdown list of models available under the selected provider. Each model will list with the input cost and the output cost.
   - **Modes**: Select one or more modes in which the model should be used. This is a multi-select field, allowing you to choose multiple modes for a single model.
  <img src="./enterprise-images/addmode.png" alt="provider" /> 
5. Click Add to include the model in your BYOK model list.
  <img src="./enterprise-images/add model.png" alt="provider" />
6. Click “Manage Default Settings”. 
7. In the form: 

  - **Chat Default Model:** Select model  for Chat from dropdown list. 

  - **Apply Default Model:** Select model  for Apply from dropdown list. 

  - **Edit Default Model:** Select model  for Edit from dropdown list. 

  - **Autocomplete Default Model:** Select model  for Autocomplete from dropdown list. 
8. Click “Update” to set default  model in your enterprise model list.
   <img src="./enterprise-images/managedefault.png" alt="provider" /> 



## Validation

- **LLM Keys**: New provider appears in Models dropdown.
- **Models Added**: Visible in enterprise list with correct cost/mode tags.
- **Defaults Applied**: New chat/edit session uses selected default model.



## Troubleshooting

- **Provider not showing in model list**  
  → API key invalid or expired  
  → **Fix**: Re-paste fresh key; test via provider dashboard first

- **Model says “Unavailable” or “Not Found”**  
  → Model not supported by provider or wrong region  
  → **Fix**: Confirm model name/ID; check provider docs

- **Default model not applying**  
  → Cache or user override in settings  
  → **Fix**: Clear browser cache; check User Preferences

- **“Invalid API Key” error on save**  
  → Key copied with extra spaces or line breaks  
  → **Fix**: Paste into notepad first, recopy cleanly

- **No modes available for model**  
  → Model doesn’t support Chat/Edit/etc.  
  → **Fix**: Choose compatible model (e.g., gpt-4o supports all modes)
