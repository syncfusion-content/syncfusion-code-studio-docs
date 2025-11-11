---
title: Using the HelpBot Context in Syncfusion Code Studio
description: Learn how to use the HelpBot context in Syncfusion Code Studio to get instant access to documentation, API references, forums, and help articles directly inside your editor.
platform: syncfusion-code-studio
keywords: code, syncfusion, helpbot, context, ai-assistance, documentation, api-reference, developer-tools
---
# HelpBot

## Purpose
The HelpBot context in Syncfusion Code Studio gives quick access to Syncfusion’s documentation. It checks user guides, API references, help articles, and forums to find useful information. This makes it easier to solve problems and understand Syncfusion documentation without leaving the editor.

## When to Use
- You want instant, documentation-powered answers for Syncfusion products without leaving your editor or searching docs manually.  
- You need help with APIs, usage examples, best practices, or troubleshooting based on the latest Syncfusion resources.

## Prerequisites
- Syncfusion Code Studio open with chat.  

## Steps

### 1. Select Helpbot Context
- In the Code Studio chat window, click the @ button. A menu will appear—select Helpbot.
> **Note:** If you cannot locate the Helpbot context option in the list, you will need to add it manually by including this context provider in the config.yaml file. Please follow the steps outlined in this [link](/code-studio/features/context-providers/add-more-contextproviders/how-to-configure-more-contextproviders) to do so.


### 2. Use Helpbot Context with Query
- After choosing the HelpBot context, you can type a question to get helpful info from Syncfusion’s documentation.  
- For example, you can ask something like “How to add Title and Content slide in PowerPoint library?” Then press Enter.  
- HelpBot will search the documentation, retrieve relevant information, and display helpful results, giving you accurate answers based on your query.  
- Results are typically fast since queries are limited to Syncfusion’s own documentation. Complex or broad queries may take slightly longer if many resources match.

<img src="../feature-images/helpbotcontext.gif" alt="helpbot" />

## Validation
- Ask for an example using a specific Syncfusion library in HelpBot context; confirm the answer references docs or shows code snippets from official sources.

## Troubleshooting
- **No useful answer**: restate your query more specifically, mentioning product, platform, or version; try a different Syncfusion control or topic.  
- **Slow/fuzzy results**: narrow your question or specify the relevant API/component for faster matching.
