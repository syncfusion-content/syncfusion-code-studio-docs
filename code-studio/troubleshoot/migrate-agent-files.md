---
title: How to Migrate Agent Files from v1.x.x to v2.0.0+
Description: Explains how to migrate Agent files from Code Studio v1.x.x to v2.0.0 and later versions by renaming the Agent file to agents.md and enabling the required Agents settings.
platform: syncfusion-code-studio
keywords: Syncfusion Code Studio, agent rules, Agent MD, agents.md, troubleshoot
---

# How to Migrate Agent Files from v1.x.x to v2.0.0+

This guide explains how to migrate Agent files from Code Studio v1.x.x to v2.0.0 and later versions so they remain compatible with the updated settings.

## Problem Summary
After upgrading to Code Studio v2.0.0 and later versions, Agent rules may stop working unless you rename your Agent files and update the **Agents** settings.

> **Note:** Agent files from v1.x.x aren’t migrated automatically in v2.0.0+. To restore Agent rules, follow the resolution steps below. Refer to the [v2.0.0 release notes](/code-studio/release-notes/v2.0.0) for migration details.

## Resolution Steps

### Step 1: Rename Your Agent File
Rename your file from `agent.md` to `agents.md` (plural) in your project root directory.

### Step 2: Update Settings Configuration

**Settings in v2.0.0 and later versions:**
1. Click the Settings icon.

    <img src="./troubleshoot-images/settings-icon.png" alt="settings icon">

2. Open Settings

    <img src="./troubleshoot-images/open-settings.png" alt="open settings">

3. In the settings window, select **Agents** in the sidebar.

    <img src="./troubleshoot-images/agent-tab-settings.png" alt="agent tab settings">

4. Ensure **Agent Enabled** and **Use Agents Md file** are enabled.

**Tip:** Keep your agent instructions under 500 lines to avoid context length issues.


