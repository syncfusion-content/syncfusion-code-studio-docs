---
title: Using the Docs Context in Syncfusion Code Studio
description: Learn how to use the Docs context provider to reference content from documentation sites directly in Syncfusion Code Studio.
platform: syncfusion-code-studio
keywords: code, syncfusion, docs-context, documentation, ai-assistance, developer-tools, productivity
---

# Docs 

The Docs context provider lets you easily reference content from any documentation site directly within Syncfusion Code Studio, making it more efficient to get help and insights based on the documents you're working with.



## How to Use the Docs context

### 1. Open the Syncfusion Code Studio

In the Syncfusion Code Studio, the chat interface is located on the left-hand side. This is where you can interact with AI and ask questions or get assistance.

<img src="../feature-images/open_chat.png" alt="Accept Image"  />

### 2. Select Docs context

In the chat window, click the `@` button and select Docs from the menu. 
> **Note:** If you cannot locate the Docs context option in the list, you will need to add it manually to include this context provider in config.yaml file. Please follow the steps outlined in this [link](https://help.syncfusioncody.com/syncfusion-code-studio/features/context-providers/add-more-contextproviders/How-to-configure-more-contextproviders) to do so. 

<img src="../feature-images/click-context.png" alt="Accept Image"  />  



Click **Add Docs**, enter the title and URL, then click **Add** to save it.

<img src="../feature-images/docs-opencontext.png" alt="Accept Image"  />

<img src="../feature-images/docs-adddocs.png" alt="Accept Image"  />

<img src="../feature-images/docs-enterdetails.png" alt="Accept Image"  />

Syncfusion Code Studio generates embeddings from chunked content and stores them locally.


<img src="../feature-images/docs-loading.png" alt="Accept Image"  />

### 3. Use Docs Context with Query

The document will appear in the list—select the one you want to use.

<img src="../feature-images/docs-choose.png" alt="Accept Image"  />

Press Enter, and the AI will respond based on the selected documentation and query.

<img src="../feature-images/docs-output.png" alt="Accept Image"  />
