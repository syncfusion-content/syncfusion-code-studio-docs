---
title: Using the Files Context in Syncfusion Code Studio
description: Learn how to use the Files context feature in Syncfusion Code Studio to provide AI with document-specific context for more accurate assistance.
platform: syncfusion-code-studio
keywords: code, syncfusion, files, context, code-studio, documentation, developer-tools, AI, productivity
---

# Files 

The Files context feature is a key component of Syncfusion Code Studio. It allows you to include relevant content from selected documents directly in the chat, enabling the AI to deliver responses that are more accurate and aligned with your files.


##  How to Use the Files context

### 1. Open Syncfusion Code Studio

In the  Syncfusion Code Studio, the chat interface is located on the left-hand side of the screen, where you can interact with the AI and get assistance.

<img src="../feature-images/open-chat.png" alt="Accept Image"  />

### 2. Select Files context

In the chat window, click the `@` button.
> **Note:** If you cannot locate the files context option in the list, you will need to add it manually to include this context provider in config.yaml file. Please follow the steps outlined in this [link](/code-studio/features/context-providers/add-more-contextproviders/how-to-configure-more-contextproviders) to do so.

<img src="../feature-images/click-context.png" alt="Accept Image"  />

A menu will appear—select Files from the list.

<img src="../feature-images/file-opencontext.png" alt="Accept Image"  />



### 3. Choose the File

After selecting Files, choose the document you want to include in context. 

<img src="../feature-images/file-choose.png" alt="Accept Image"  />


### 4. Use file Context with Query

Type a relevant query about the selected file in the chat box and press Enter.
Syncfusion Code Studio will read and analyze the selected file(s), allowing the AI to provide more context-aware and helpful responses based on the content of your files and the query you've submitted.
<img src="../feature-images/file-output.png" alt="Accept Image"  />
