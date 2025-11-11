---
title: Using the Terminal Context in Syncfusion Code Studio
description: Learn how to use the Terminal context in Syncfusion Code Studio to debug and resolve terminal errors efficiently with AI-powered suggestions.
platform: syncfusion-code-studio
keywords: code, syncfusion, terminal, context, ai-assistance, debug, terminal-errors, developer-tools
---

# Terminal

## Purpose
The Terminal context in Syncfusion Code Studio helps you fix errors shown in your terminal. It reads the latest output from the terminal and gives helpful suggestions or solutions based on what it finds. This makes it easier to understand and solve terminal issues quickly.

## When to Use
- You want the assistant to analyze recent terminal output (build logs, test failures) without pasting it into chat.  
- You’re facing package install issues, or failing scripts and need targeted guidance.

## Prerequisites
- Syncfusion Code Studio open with a project.  

## Steps

### 1. Select Terminal Context
- In the Code Studio chat window, click the @ button. A menu will appear—select Terminal.  
> **Note:** If you cannot locate the Terminal context option in the list, you will need to add it manually by including this context provider in the config.yaml file. Please follow the steps outlined in this [link](/code-studio/features/context-providers/add-more-contextproviders/how-to-configure-more-contextproviders) to do so.

> **Note:** Before using the terminal context, ensure that you have opened a terminal in VS Code and that it contains relevant information or error details necessary for proper functionality.

### 2. Use Terminal Context with Query
- After choosing terminal context, input relevant details about the issue in the chat model window and click Enter.  
- The AI will process the terminal data and present you with suggestions or solutions directly in the chat window. Review these recommendations to address the issue or error at hand.  
- Very long logs increase token usage and latency. Trim to the error section or rerun the command with reduced verbosity when possible.

<img src="../feature-images/terminalcontext.gif" alt="terminal" />

## Validation
- Run a command that fails. Select @Terminal and ask for a diagnosis; confirm the response references the logged error.  
- Switch to another terminal and repeat; verify the assistant analyzes the selected terminal’s output.

## Troubleshooting
- **Multiple errors interleaved**: select the terminal with the specific failure, or share a smaller slice around a single error for clarity.
