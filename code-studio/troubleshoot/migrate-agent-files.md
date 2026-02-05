---
title: How to Migrate Agent Files from Prior Versions to the Current Release?
Description: Explains how to migrate Agent Markdown instructions from older Code Studio versions to v2.0.0+ by renaming the Agent file to agents.md and enabling Agent file usage in the updated Agents settings.
platform: syncfusion-code-studio
keywords: Syncfusion Code Studio, agent rules, Agent MD, agents.md, troubleshoot
---

# How to Migrate Agent Files from Prior Versions to the Current Release

This guide explains how to migrate Agent Markdown files from prior versions so they work in Code Studio v2.0.0+.

## Problem Summary
After upgrading to Code Studio v2.0.0+, Agent rules from earlier versions may not apply until you migrate your Agent file naming and update the new **Agents** settings.

## Resolution Steps

### Step 1: Rename Your Agent File
Rename your file from `agent.md` to `agents.md` (plural) in your project root directory.

### Step 2: Update Settings Configuration
The settings location has changed in the current release:

**Prior Version Settings:**
- Go to Settings menu → Chat category
- Toggle "Enable/Disable Agent Rules"

**Current Release Settings:**
1. Click the Settings Icon 

<img src="./troubleshoot-images/settings-icon.png" alt="settings icon">

2. Open Settings

<img src="./troubleshoot-images/open-settings.png" alt="open settings">

3. Now, Code Studio settings will be opened. Select  Agents in the sidebar. 

<img src="./troubleshoot-images/agent-tab-settings.png" alt="agent tab settings">

4. Make sure  Agent Enabled Option and Use Agents Md file Options  are enabled. 

**Note**: Keep your agent instructions under 500 lines to avoid context length issues.


