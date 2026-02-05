---
title: Syncfusion Code Studio User Settings Reference
description: "Professional guide for customizing development environment settings and optimizing workflow efficiency"
classification: "User Guide - Configuration Documentation"
platform: syncfusion-code-studio
keywords: user-settings, customization, configuration, development-environment, workflow-optimization
---

# User Settings

## Purpose

Settings allow users to tailor the development environment to their individual preferences. They help by providing:

- **Centralized Control** – All key configuration options are available in one place.
- **Personalization** – Customize features such as agents, autocomplete, and instructions to fit your workflow.
- **Usage Monitoring** – Track daily costs and token usage to stay within budget.
- **Compliance & Transparency** – Access legal policies, agreements, and telemetry settings for clarity.
- **Help & Support** – Quickly reach documentation, tutorials, and support tickets when needed.

## When to Use

- You want consistent behavior across projects via explicit settings.
- You need to enable agents, inject instructions, or tune request limits.
- You monitor usage/costs or manage credits and subscriptions.
- You prefer to adjust autocomplete, indexing, or telemetry policies.

## Prerequisites

- Syncfusion Code Studio installed and a project folder opened with write access. If you have not yet downloaded Code Studio, see the [installation guide](/code-studio/getting-started/install-and-configuration).

## How to Access User Settings

The User Settings page can be accessed in three ways:

### 1. From the Account

- Click the Code Studio Account icon.

<img src="../reference-images/settings-account.png" alt="UserSettings" >

- The Settings page will open.

<img src="../reference-images/settings-page-chat.png" alt="UserSettings" >

### 2. From the Toggle Sidebar

- Click the **gear icon** on the left sidebar of the Code Studio window.
- Select Code Studio Settings from the menu.

<img src="../reference-images/settings-sidebar.png" alt="UserSettings" >

- The Settings page will open.

<img src="../reference-images/settings-page-chat.png" alt="UserSettings" >

### 3. From the Chat Window

- Navigate to the **Code Studio Chat Window**.
- Click the **gear icon** located at the top right corner.
- Select Open Settings. 

<img src="../reference-images/settings-chat-window.png" alt="UserSettings" >

- The settings page will open.

<img src="../reference-images/settings-page-chat.png" alt="UserSettings" >

## Settings Categories

The following settings are available on the User Settings page.


### Account

#### Manage Account
  - Monitor your LLM usage and manage billing and subscriptions.

> **Note:** You can track daily costs and token usage by applying filters in your Dashboard. This helps you stay on budget and manage usage effectively.

#### Upgrade to Pro Plan
  - Upgrade to the Pro plan for additional features.

> **Note:** Only admins can upgrade.

#### Email 
  - Sign in or sign out of your account.

<img src="../reference-images/settings-page.png" alt="UserSettings" >

### Credits

- View your current balance. 
- Purchase credit based on your budget and requirements. 
- Access pricing details. 

> **Note:** The Credits section is accessible only to admins. 

<img src="../reference-images/settings-credits.png" alt="UserSettings" >

### Agents

#### Agent Enabled 
- Enables agent mode, which can be activated via the dropdown in the chat box. 
- Default: Enabled 

#### Agent Max Requests 
- Sets the maximum number of requests per turn when using an agent. If the limit is reached, you’ll be asked to confirm to continue. 
- Default: 25 

#### Use AGENTS.md File 
- Decide whether the instructions from the AGENTS.md file in your workspace are added to every chat request.
- Default: Enabled.

<img src="../reference-images/settings-agents.png" alt="UserSettings" >

### Instructions

#### Use codestudio-instructions.md File 
- Controls whether instructions from `.codestudio/codestudio-instructions.md` are added to Code Studio requests. 

> **Note:** Keep your instructions short and precise. Poor instructions can degrade Code Studio quality and performance. 

#### Instruction File Locations 
- Specify locations of instruction files (`*.instructions.md`) that can be attached in chat sessions.

<img src="../reference-images/settings-instruction.png" alt="UserSettings" >

### Autocomplete

- When enabled, Code Studio provides inline code suggestions across all supported languages.

<img src="../reference-images/settings-autocomplete.png" alt="UserSettings" >

### Indexing

- When enabled, Code Studio will start an indexing process to scan and embed workspace files for accurate search results. 

<img src="../reference-images/settings-indexing.png" alt="UserSettings" >

### Telemetry

- When enabled, Code Studio collects anonymous telemetry data to improve the product. 

<img src="../reference-images/settings-telemetry.png" alt="UserSettings" >

### Help & Support

- **Documentation**  
  Access the official Syncfusion Code Studio documentation for configuration guidance and usage instructions.

- **Have an Issue?**  
  If you encounter any problems, you can easily reach out to our support team at [support@syncfusion.com](https://support.syncfusion.com).

- **Legal Center**  
  Review our transparent legal policies and agreements in the Legal Center. This ensures you fully understand and comply with Syncfusion’s terms and conditions. 
