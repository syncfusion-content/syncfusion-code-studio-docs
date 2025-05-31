---
title: Using the @Docs Context in Syncfusion Code Studio
description: Learn how to use the @Docs context provider to reference content from documentation sites directly in Syncfusion Code Studio.
platform: syncfusion-code-studio
keywords: code, syncfusion, docs-context, documentation, ai-assistance, developer-tools, productivity
---

# @Docs Context Feature Overview

The @Docs context provider lets you easily reference content from any documentation site directly within Syncfusion Code Studio, making it more efficient to get help and insights based on the documents you're working with.



## How to Use the @Docs Context

### 1. Open the Syncfusion Code Studio

In the Syncfusion Code Studio, the chat interface is located on the left-hand side. This is where you can interact with AI and ask questions or get assistance.

<img src="../feature-images/files1.png" alt="Accept Image" width="100%" height="auto" />

### 2. Select @Docs context

In the chat window, click the “@” button and select @Docs from the menu.  

<img src="../feature-images/files2.png" alt="Accept Image" width="100%" height="auto" />  

**Note:**   If you cannot locate the @Docs context option in the list, you will need to add it manually to include this context provider in config.yaml file. Please follow the steps outlined in this [link](/syncfusion-cody/features/context-providers/add-more-contextproviders/How-to-configure-more-contextproviders.md) to do so.

Click **Add Docs**, enter the title and URL, then click **Add** to save it.

<img src="../feature-images/docs1.png" alt="Accept Image" width="100%" height="auto" />

<img src="../feature-images/docs3.png" alt="Accept Image" width="100%" height="auto" />

<img src="../feature-images/docs2.png" alt="Accept Image" width="100%" height="auto" />

Syncfusion Code Studio generates embeddings from chunked content and stores them locally.


<img src="../feature-images/docs4.png" alt="Accept Image" width="100%" height="auto" />

### 3. Use @Docs Context with Query

The document will appear in the list—select the one you want to use.

<img src="../feature-images/docs5.png" alt="Accept Image" width="100%" height="auto" />

Press **Enter**, and the AI will respond based on the selected documentation and query.

<img src="../feature-images/docs6.png" alt="Accept Image" width="100%" height="auto" />
