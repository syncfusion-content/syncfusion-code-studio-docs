---
title: Using the Web Context in Syncfusion Code Studio
description: Learn how to use the Web context feature in Syncfusion Code Studio to access real-time web content for the most current and accurate AI responses.
platform: syncfusion-code-studio
keywords: Syncfusion Code Studio, syncfusion, web, context, code-studio, real-time, AI, developer-tools, productivity
---
 
# Web 
 
## Purpose
The Web context provider in Syncfusion Code Studio allows the AI to access real-time web content, ensuring responses are accurate, current, and context-aware.

## When to Use
- You need current, real-time information from the public web (latest versions, changelogs, advisories, tutorials).  
- You want the assistant to cite specific pages it searched so you can verify the answer.  
- You prefer not to copy/paste content; the provider fetches and summarizes relevant pages for you.

## Prerequisites
- Syncfusion Code Studio open with chat.

## Steps

### 1. Select Web Context
- In the Code Studio chat window, click the @ button. A menu will appear—select Web.  
> **Note:** If you cannot locate the Web context option in the list, you will need to add it manually to include this context provider. Please follow the steps outlined in this [link](/code-studio/features/context-providers/add-more-contextproviders/how-to-configure-more-contextproviders) to do so.

### 2. Use Web Context with Query
- After selecting the Web context provider option, type your query for which you want the AI to provide the latest up-to-date information.  
- Now, the web context provider will give the response from the latest web content and display the context items that are passed to the AI model, providing up-to-date information for the conversation.

<img src="../../feature-images/webcontext.gif" alt="web" />

## Validation
- Ask for a recent framework release summary; verify the response includes linked sources.  
- Refine the query with a domain filter and confirm sources match.

## Troubleshooting
- **Web option missing**: enable the provider in config.yaml and reload.  
- **Results seem generic**: add domain filters or specify version/platform.