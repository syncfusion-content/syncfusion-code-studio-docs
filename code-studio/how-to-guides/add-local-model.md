---
title: How to Add BYOK Models using your own API Key
description: Learn how to add and manage your own AI models in Code Studio using API keys from providers like OpenAI and Anthropic.
platform: syncfusion-code-studio
keywords: how-to, BYOK, personal-models, API-keys
---

# How to add BYOK Models using your own API Key

## Overview

Bring Your Own Key(BYOK) models in Code Studio allow you to integrate AI models from various providers using your own API keys. This feature gives you access to specific models that may not be available in your organization's configuration. You can add, manage, and use these models alongside your organization's models for enhanced flexibility and experimentation.

## When to Use

Use BYOK models when you need to:

- Experiment with specific models for personal projects
- Access models when they are not available in your organization’s configuration
- Compare different providers and model capabilities
- Match models to unique coding or cost requirements

## Prerequisites

- Valid API keys from your chosen provider (e.g., OpenAI, Anthropic)
- Active provider account with sufficient credits or quota

## How To Add a BYOK Model?

1. Click the model’s section dropdown and select `Manage Models`.

   <img src="howtoguide-images/manageModels.png" alt="Manage Models">

2. A Language Models page will open. This page provides information about the configured Providers and their models in CodeStudio.

   <img src="howtoguide-images/LanguageModels.png" alt="LanguageModels">

3. Click the **Add Models** button. Choose your preferred provider from the list (for example: OpenAI, Anthropic).

   <img src="howtoguide-images/LanguageProviders.png" alt="LanguageProviders">

4. Enter the Group Name. The group name is used to organize and display a set of models under a specific provider, based on the associated API key.

   <img src="howtoguide-images/GroupName.png" alt="GroupName">

5. Enter your API Key for the selected provider.

   <img src="howtoguide-images/ProviderAPIKey.png" alt="API Key">

   > **Note:** Ensure the API key is valid and correct.

4. After adding the API key, the available models will be listed. 

   <img src="howtoguide-images/ModelsList.png" alt="Models">

5. To add models to the Chat Model Picker:

   1. Hover over the model name on the left side.
   2. An eye icon will appear.
   3. Toggle the eye icon to add or remove the model from the Chat Model Picker.

      <img src="howtoguide-images/AddOrRemoveModels.gif" alt="Choose Model">

6. The added models will appear under `Other Models`. You can use them in the same way as any built-in or organization-configured model.

   <img src="howtoguide-images/BYOKModelsinPicker.png" alt="Other Model">

## How to edit the Group Name and API Key for a configured provider?

1. Click the Settings icon.
2. Select Configure. A UI will appear where you can edit the Group Name and API Key.

   <img src="howtoguide-images/Edit-the-BYOKModels.gif" alt="Edit Provider">

## How to Remove a Provider?

1. Click the Settings icon.
2. Select the Delete option. A confirmation popup will appear — click Yes to complete the removal.

   <img src="howtoguide-images/RemoveProvider.png" alt="Remove Provider">

## Tips

- Use separate API keys for personal and organizational work
- Prefer lightweight models for small tasks to manage costs
- Keep API keys secure and never commit them to repositories
- Test models on small tasks first to understand behavior
- Remove unused models to keep the workspace organized
