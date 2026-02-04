---
title: Syncfusion Code Studio Inline Chat
description: "Professional guide for AI-powered inline code editing and contextual modifications"
classification: "User Guide - Feature Documentation"
platform: syncfusion-code-studio
keywords: inline-edit, right-click-actions, ai-assistance, contextual-editing, code-optimization
---


# Inline Chat in Syncfusion Code Studio

## Overview
Inline Chat in Syncfusion Code Studio is designed to bring AI assistance directly into your workflow. Instead of switching panels or navigating away from your code, you can interact with AI right inside the editor or terminal. This seamless integration helps you stay focused, get context-aware suggestions, and streamline both coding and command-line tasks.

## Use Cases
- Debugging Code Quickly – Use Inline Chat to identify errors and generate fixes directly in the editor without switching panels. 

- Automating Terminal Workflows – Generate shell commands or scripts in the integrated terminal to speed up repetitive tasks. 

- Refactoring Existing Code – Select a block of code and request improvements, optimizations. 

## Prerequisites 

- Syncfusion Code Studio installed and configured on your system. If you have not yet downloaded Code Studio, please refer to this link [Install and Configure](/code-studio/getting-started/install-and-configuration) for step-by-step instructions on downloading and configuring Code Studio.

## Using Inline Chat in the Editor
When you use Inline Chat inside the editor, Code Studio scopes your request to the content in the active file. It may also use related files in your workspace to provide more accurate suggestions.

### How to Use Editor Inline Chat
**Steps:**
1. **Open a file** in the Code Studio editor.
2. Open Inline Chat by doing one of the following:
   - Press `Ctrl + I`
   - Or **Right-click** inside the editor → **Open Inline Chat**

   <img src="./feature-images/inlinechat1.png" alt="inlinechat"  />
   

3. Type your request in the inline chat input box and press **Enter** to submit.

   <img src="./feature-images/Gif/inlinechat2.gif" alt="inlinechat"  />

> **Tip:** Select a block of code before opening Inline Chat if you want AI to focus on that part.

### Reviewing Suggestions
After processing your request, Code Studio shows an inline diff view. You can:
- **Keep** the changes
- **Undo** the changes

  <img src="./feature-images/inlinechat3.png" alt="inlinechat"  />


## Using Inline Chat in the Terminal
Terminal Inline Chat helps you work with shell commands, scripts, and terminal workflows directly inside Code Studio’s integrated terminal.

### How to Use Terminal Inline Chat
**Steps:**
1. Open the terminal (**View → Terminal** or `Ctrl + ```).
2. Start Terminal Inline Chat using `Ctrl + I`.
3. Type your command request and press **Enter**.

   <img src="./feature-images/Gif/inlinechat4.gif" alt="inlinechat"  />

### Running or Inserting Commands
After Code Studio generates a shell command:
- Select **Run (Ctrl + Enter)** to execute immediately
- Select **Insert (Alt + Enter)** to add it into the terminal for editing

   <img src="./feature-images/inlinechat5.png" alt="inlinechat"  />

## Releted Features
- [Add context to your chat prompt](/code-studio/features/add-context) - Enhance your prompt by providing extra details. This helps Code Studio generate more accurate results and keeps your workspace aligned with your goals.



