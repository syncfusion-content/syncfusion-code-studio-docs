---
title: Using the Database Context in Syncfusion Code Studio
description: Learn how to use the Database context feature in Syncfusion Code Studio to integrate database schema and enable data-aware AI conversations.
platform: syncfusion-code-studio
keywords: syncfusion, syncfusion Code Studio, database, context, code-studio, data-driven, AI, developer-tools, productivity
---
 
# Database 
 
## Purpose 
The Database context option in Syncfusion Code Studio enables users to add database-related information directly into the chat, making it easier to access data during development.

## When to Use
- To get accurate AI assistance or suggestions based on real database structure.
- When you need to compose, explain, or troubleshoot SQL queries with schema context.

## Prerequisites
- Syncfusion Code Studio open 
- Access to the target database including credentials.
 
## Steps
 
### 1. Open the Syncfusion Code Studio
 
- In the Syncfusion Code Studio, the chat interface is located on the left-hand side. This is where you can interact with AI and ask questions or get assistance.

<img src="../../feature-images/open-chat.png" alt="open chat" />
 
### 2. Select Database context
 
- In the chat window, click the `@` button.  
> **Note:** If you cannot locate the Database context option in the list, you will need to add it manually to include this context provider. Please follow the steps outlined in this [link](/code-studio/features/context-providers/add-more-contextproviders/how-to-configure-more-contextproviders) to do so.

<img src="../../feature-images/click-context.png" alt="Clickcontext" />
 
A menu will appear—select Database context option to view the list of table schema.

<img src="../../feature-images/Databaseselect.png" alt="opencontext" />
 
### 3. Select Required Table Schema
 
- Select the table schemas from the list to enable the AI to access the connected database and deliver accurate, data-driven responses.
<img src="../../feature-images/database-choose.png" alt="output" />

 
### 4. Describe the Query
 
- Input relevant details about the query in the chat model window and click Enter.  
- The AI will generate the response based on the context datas.

<img src="../../feature-images/database-output.png" alt="output" />

## Validation
- Ensure table schemas are listed after choosing the database context.
- Ensure selected table schemas enable the AI to deliver precise, informed responses.


## Troubleshooting
- **Unable to View Table Schemas**: Ensure you have correct credentials and necessary database read permissions.Verify the connection details and database availability.