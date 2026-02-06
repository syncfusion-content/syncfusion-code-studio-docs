---
title: How to Add Personal Models
description: Learn how to add and manage your own AI models in Code Studio using API keys from providers like OpenAI and Anthropic.
platform: syncfusion-code-studio
keywords: how-to, BYOK, personal-models, API-keys
---

# Add Models for Personal Use

## Overview

Personal models in Code Studio allow you to integrate AI models from various providers using your own API keys. This feature gives you access to specific models that may not be available in your organization's configuration. You can add, manage, and use these models alongside your organization's models for enhanced flexibility and experimentation.

## When to Use

Use personal models when you need to:

- Experiment with specific models for personal projects
- Access models when they are not available in your organization’s configuration
- Compare different providers and model capabilities
- Match models to unique coding or cost requirements

## Prerequisites

- Valid API keys from your chosen provider (e.g., OpenAI, Anthropic)
- Active provider account with sufficient credits or quota

## How To Add a Personal Model?

1. Click the model’s section dropdown and select `Manage Models`.

   <img src="how-to-guides-images/manageModels.png" alt="Manage Models">

2. Choose your preferred Provider (e.g., OpenAI, Anthropic).

   <img src="how-to-guides-images/selectProvider.png" alt="Select Providers">

3. Enter your API Key for the selected provider.

   <img src="how-to-guides-images/apiKey.png" alt="API Key">

   > **Note:** Ensure the API key is valid and correct.

4. After adding the key, available models will be listed. Choose the models you want from the list.

   <img src="how-to-guides-images/modelList.png" alt="Models">

5. Click `OK` to add the selected model(s).

   <img src="how-to-guides-images/clickOk.png" alt="Choose Model">

6. The added models appear under `Other Models`. You can use them like any built‑in or organization‑configured model.

   <img src="how-to-guides-images/otherModels.png" alt="Other Model">

## How To Remove a Personal Model?

1. Open `Manage Models` from the model’s dropdown section.

   <img src="how-to-guides-images/manageModels.png" alt="Manage Models">

2. Select the Provider (e.g., OpenAI, Anthropic).

   <img src="how-to-guides-images/selectProvider.png" alt="Select Providers">

3. Uncheck the model you want to remove and click `OK`.

   <img src="how-to-guides-images/modelList.png" alt="Remove Model">

## Tips

- Use separate API keys for personal and organizational work
- Prefer lightweight models for small tasks to manage costs
- Keep API keys secure and never commit them to repositories
- Test models on small tasks first to understand behavior
- Remove unused models to keep the workspace organized
