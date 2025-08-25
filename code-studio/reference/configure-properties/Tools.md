---
title: Introduction to Tools in Syncfusion Code Studio
description: Learn how to use the built-in tools in Syncfusion Code Studio to streamline your development workflow and automate tasks efficiently.
platform: syncfusion-code-studio
keywords: tools, syncfusion, code-studio, development, automation, workflow, built-in-tools
---

# Tools
## Overview
 The Tools feature in Syncfusion Code Studio empowers developers to perform specific actions within the development environment, such as creating folders, reading files, searching within files, and interacting with browsers. This guide provides a step-by-step approach to use the built-in tools, enabling you to streamline your development workflow and automate tasks efficiently with simple prompts.

## Purpose

The built-in tools are designed to automate and simplify common development tasks, allowing you to focus on writing code. Key purposes include:

### 1. File Management
- Create new files or edit existing ones.
- Perform bulk search-and-replace operations.
- Organize project structures efficiently.
### 2. Terminal Integration
- Run CLI commands like npm install or yarn start.
- Install dependencies or launch development servers.
- Automate build and deployment processes.
### 3. Code Insights
- Identify and fix bugs with AI-driven suggestions.
- Refactor code for better performance or readability.
- Generate inline documentation automatically.
### 4. Web and Browser Tools
- Perform web searches to fetch relevant resources.
- Automate browser tasks like testing or scraping.

## Built-In Tools

Syncfusion Code Studio provides a suite of tools to streamline your workflow. Below is a comprehensive list of available tools, their descriptions, and example usage.
 
### 1. Ensure the Required Tools Policy

To balance speed and safety, each tool in Syncfusion Code Studio can be configured in one of three modes:
- **Automatic:** When the model requests a tool, Code Studio automatically executes it and sends the response back to the model.
- **Ask First:** When the model requests a tool, Code Studio prompts you to either "Cancel" or "Continue" before proceeding.
- **Excluded:** The model is unaware of the tool and cannot use it.

 To change the mode, click on the desired option. Once configured, enter your prompt to perform the task. Code Studio will then leverage the selected tools to build the application.
### 2. Toolset Overview

The following table lists all available built-in tools and their descriptions:
| Tool Name | Description |
|-----------|-------------|
| `builtin_read_file` | Reads the contents of an existing file. |
| `builtin_create_new_file` | Creates a new file with specified content. |
| `builtin_run_terminal_command` | Executes a terminal command in the current directory. |
| `builtin_grep_search` | Performs a fast text search using exact strings or regex. |
| `builtin_file_glob_search` | Searches for files matching a glob pattern, returning their paths. |
| `builtin_search_web` | Conducts a web search and returns top results. |
| `builtin_view_diff` | Displays the diff of current working changes. |
| `builtin_read_currently_open_file` | Reads the contents of the currently open file in the IDE. |
| `builtin_ls` | Lists files and folders in a specified directory. |
| `builtin_syncfusion_ui_builder` | Generates Syncfusion component metadata or UI layout plans. |
| `builtin_browser_interaction` | Automates browser tasks using a Puppeteer-controlled environment. |
| `builtin_replace_in_file` | Makes targeted edits to specific parts of a file. |
| `builtin_search_files` | Searches for regex patterns within specified files. |

## How to Use Tools

1. **Open the Chat Window** - Click the Syncfusion Code Studio icon on the left toolbar to open the chat interface.

2. **Enter Your Request** - Type your request in natural language, describing what you want to accomplish. Ensure code Studio is in Agent mode.

3. **Review Tool Execution** - The AI will automatically select and execute the appropriate tools based on your request.

4. **Approve Changes** - Review any proposed changes and approve or modify them as needed.

<img src="../reference-images/Tools.gif" alt="Tools" >



