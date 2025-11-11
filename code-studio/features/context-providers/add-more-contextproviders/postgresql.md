---
title: Using the PostgreSQL Context in Syncfusion Code Studio
description: Learn how to use the PostgreSQL context feature in Syncfusion Code Studio to interact with PostgreSQL databases directly from your development environment.
platform: syncfusion-code-studio
keywords: syncfusion, syncfusion Code Studio, postgresql, database, context, code-studio, AI, developer-tools, productivity
---
 
# PostgreSQL 
 
## Purpose
The PostgreSQL context provider in Syncfusion Code Studio enables seamless integration with PostgreSQL databases, allowing you to interact with your database directly from your development environment.

## When to Use
- When you want to analyze, query, or get help with your PostgreSQL database from within your development workflow.
- To make AI recommendations more relevant by supplying real database schema and data context.

## Prerequisites
- Syncfusion Code Studio open 
- Access to a PostgreSQL database with necessary credentials (hostname, port, database, user, password).
 
## Steps
 
### 1. Open the Syncfusion Code Studio
 
- In the Syncfusion Code Studio, the chat interface is located on the left-hand side. This is where you can interact with AI and ask questions or get assistance.

<img src="../../feature-images/open-chat.png" alt="openchat" />
 
### 2. Select PostgreSQL context
 
- In the chat window, click the `@` button.  
> **Note:** If you cannot locate the PostgreSQL context option in the list, you will need to add it manually to include this context provider. Please follow the steps outlined in this [link](/code-studio/features/context-providers/add-more-contextproviders/how-to-configure-more-contextproviders) to do so.
 
<img src="../../feature-images/click-context.png" alt="click context" />

A menu will appear—select PostgreSQL. This allows the AI to access your PostgreSQL database and utilize its data for context.

<img src="../../feature-images/postgres-opencontext.png" alt="opencontext" />
 
### 3. Select Required Table Schema
 
- Select the table schemas from the list to enable the AI to access the connected database and deliver accurate, data-driven responses.

<img src="../../feature-images/postgres-choose.png" alt="choose" />
 
### 4. Describe the Query
 
- Give the detailed query in the chat model window and click Enter.  
- The AI will provide responses based on the PostgreSQL database context.

<img src="../../feature-images/postgres-output.png" alt="output" />

## Validation
- Ensure the PostgreSQL context option appears in the @ context menu after adding.
- Ensure you are able to select and see your PostgreSQL table schemas.
- Ensure AI responses reference accurate database schema information.


## Troubleshooting
- **Can’t Connect to Database**: Ensure correct database credentials and network accessibility.Check that the PostgreSQL service is running.
