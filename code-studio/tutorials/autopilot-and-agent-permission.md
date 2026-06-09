---
title: Autopilot and Agent Permissions
description: Learn how to control agent autonomy in chat sessions using the session‑scoped permissions picker. This tutorial explains the three permission levels — Default Approvals, Bypass Approvals, and Autopilot (Preview) — how to enable, how to attach for running agents that can perform file edits, terminal commands, or external tool calls. 
platform: syncfusion-code-studio
keywords: Autopilot; agent permissions; Default Approvals; Bypass Approvals; Autopilot Preview.
---
# Autopilot and Agent Permissions
## Overview
Code Studio’s Autopilot and Agent Permissions let you control how independently an AI agent operates during a session. This tutorial shows where to find the permissions picker in the Chat view, how to choose between Default Approvals, Bypass Approvals, and Autopilot (Preview), and when to switch levels so automation matches the task and your risk tolerance.

This flexibility ensures you can tailor agent behavior to suit routine tasks, complex projects, or anything in between.

## What You Will Learn
By following this tutorial, you will be able to:

- Understand the three permission levels and when to use each one.
- Confidently use Autopilot for longer tasks while understanding the security implications.
- Monitor agent progress and interrupt execution when needed.
- Manage common scenarios like agent auto retries and error recovery.

## Steps to Get Started
### Step 1: Understand the Three Permission Levels

Code Studio provides three permission levels. Each one offers a different balance of automation and control:

1. Default Approvals
    
    - Shows a confirmation dialog before the agent runs any significant action. You manually approve each step.
    - When to use:
        - Complex tasks where you need full visibility.   
        - When working with unfamiliar code or systems
        - First time working on a critical project and best for learning and exploration.

2. Bypass Approvals
    - Auto approve all tool calls without showing confirmation dialogs. The agent executes actions immediately, but you stay in the session and can interrupt at any time.
    - When to use:
        - Routine, repetitive tasks you trust the agent to manage.
        - Tasks where you have verified the agent's approach. Short, well-scoped work
        - When you want faster execution but do not need full automation

3. Autopilot (Preview)
    - Full autonomous operation. The agent auto approves all actions, automatically manages errors, and continues working until the task is complete. You stay informed with status updates but do not need to approve each step.

    - When to use:
        - Extended, complex projects where you want hands-off operation.
        - Well-scoped tasks on trusted, version-controlled projects
        - Work where you have already verified the approach.
        - Auto approves all tool calls, automatically retrieving failed operations. 
        - Continue iterating until the agent determines the task is complete.
        - You can still interrupt at any time by stopping the chat.

> **Note**: Bypass Approvals and Autopilot bypass manual approval prompts and ignore your configured approval settings, including potentially destructive actions like file edits, terminal commands, and external tool calls. The first time you enable either level, a warning dialog asks you to confirm. Only use these levels if you understand the security implications.

When to use these modes:
- Only on trusted projects where you understand the code. Only for short, well-scoped tasks 
- Only on local/development machines, not production systems
- When you have version control so you can revert changes

### Step 2: Access and Change Permission Levels

- Open the Chat view in Code Studio and find the permissions dropdown at the Chat below, you will see the current permission level displayed.

    <img src="./tutorials-images/chat.png" alt="Code generation demo" />

- Click the permissions picker to reveal all three available options. Each option displays:

    <img src="./tutorials-images/chat-list.png" alt="Code generation demo" />

- Click the permission level you want to use. A confirmation dialog appears the first time you select Bypass Approvals or Autopilot. Review the warning dialog, this confirms you understand the security implications of your choice. 
    <img src="./tutorials-images/bypass-warning.png" alt="Code generation demo"/>

- Click "Enable” to proceed. The Chat view updates to show your new permission level.

- The agent will operate under this permission level for the remainder of your current chat session. You can change it at any time.

- **To Disable a Permission Level** - Open the permissions picker and select Default Approvals to return to the safest mode or close the chat session and start a new one

### Step 3: Monitor Agent Progress
- The agent provides status updates as it works, showing what steps, it is taking and what it has completed.
- You can see which tools the agent is using and the output it receives.
- If the agent encounters an error, Autopilot automatically retrieves. You will see retry attempts in the Chat view.
- Interrupt Autopilot at Any Time, Click the Stop button in the Chat view or switch to a different permission level.
- The agent signals completion by calling the `task_complete` tool, which ends the autonomous iteration and returns control to you.
- Review the work, Files created or modified, terminal output and logs shown in the Chat view, Whether the results match your original request.

<img src="./tutorials-images/bypass-approval.gif" alt="Code generation demo" />

## What's Next
- Agent Debug Log — provides detailed visibility into Autopilot’s tool calls and prompts.
- [Hooks](/code-studio/reference/configure-properties/hooks)  also integrate with the Agent Debug Panel, giving visibility into what Autopilot did and why.