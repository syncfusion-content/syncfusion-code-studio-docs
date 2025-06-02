---
title: Using the Problems Context in Syncfusion Code Studio
description: Learn how to use the Problems context in Syncfusion Code Studio to fix coding issues quickly with intelligent, file-specific assistance.
platform: syncfusion-code-studio
keywords: code, syncfusion, problems, context, bug-fixing, ai-assistance, coding-errors, developer-tools
---

# Problems

The problems context in Syncfusion Code Studio makes it easier to fix problems in your code. With the problems context, you can quickly focus on specific issues found in your project. This is useful when you need help with a particular error or bug. It shows file-specific problems and lets the AI give better support based on the code you are currently looking at.



## How to Use the Problems context

### 1. Open the File

Ensure the file with the problem is open in your VS Code editor.

<img src="../feature-images/problems_file.png" alt="problems file"  />


### 2. Access the Chat Window

Open the chat model window of the Syncfusion Code Studio by clicking the Syncfusion Code Studio icon on the left toolbar.

<img src="../feature-images/problems_chat_open.png" alt="open chat" />


### 3. Select Problems context

In the chat window, click the `@` button.
> **Note:** If you cannot locate the problems context option in the list, you will need to add it manually by including this context provider in the config.yaml file. Please follow the steps outlined in this [link](https://help.syncfusioncody.com/syncfusion-code-studio/features/context-providers/add-more-contextproviders/How-to-configure-more-contextproviders) to do so.

<img src="../feature-images/problems-clickcontext.png" alt="Click context menu"  />

From the context menu that appears, choose problems.



<img src="../feature-images/problems_open_context.png" alt="open context menu" />



### 4. Use problems Context with Query

Input relevant details about the issue in the chat model window and click Enter.

The AI will analyze the problems data and offer suggestions or solutions for issues in the currently opened file directly in the chat window. This will help you resolve issues in the file you're working on in the VS Code editor.


<img src="../feature-images/problems_output.png" alt="problems response" />