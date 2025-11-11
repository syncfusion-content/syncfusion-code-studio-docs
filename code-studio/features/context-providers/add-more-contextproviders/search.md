---
title: Using the Search Context in Syncfusion Code Studio
description: Learn how to use the Search context feature in Syncfusion Code Studio to search across your codebase or documentation efficiently.
platform: syncfusion-code-studio
keywords: syncfusion, syncfusion Code Studio, search, exactsearch, context, codebase, AI, developer-tools, productivity
---
 
# Search 
 
## Purpose
The Search context option in the Syncfusion Code Studio allows users to perform precise searches across their codebase or documentation. It is particularly useful for developers and content creators who need to quickly locate specific strings, functions, or variables.

## When to Use
Use the Search context when you need to:
- Locate specific strings, functions, or variables across your codebase or documentation.
- Understand how a particular object is used throughout the project.
- Quickly navigate large projects without manually opening each file.
- Perform targeted queries without relying on open tabs.

## Prerequisites
Syncfusion Code Studio open with a project.

## Steps

### 1. Select Search Context
- In the Code Studio chat window, click the @ button.
- A menu will appear—select Search.
> **Note:** If you cannot locate the Search context option in the list, you will need to add it manually to include this context provider. Please follow the steps outlined in this [link](/code-studio/features/context-providers/add-more-contextproviders/how-to-configure-more-contextproviders) to do so.

### 2. Use Search Context with Query
- After choosing the Search context, type your query in the chat window.
- Include relevant details such as the name of the function, variable, or string you're looking for.
- Press Enter to submit.
- The AI will search your entire project and return results showing where and how the item is used.

<img src="../../feature-images/Search.gif" alt="search" />

## Validation
- Search for a known function name and verify that the AI returns all its references.
- Try searching for a string in both code and documentation to test cross-artifact coverage.

## Troubleshooting
- **Search not in @ menu:** Enable it in `config.yaml` and reload Code Studio.
- **No results returned:** Ensure the query is spelled correctly and exists in the current workspace.