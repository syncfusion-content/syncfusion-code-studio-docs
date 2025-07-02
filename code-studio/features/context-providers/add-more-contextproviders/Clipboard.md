---
title: Using the Clipboard Context in Syncfusion Code Studio
description: Learn how to use the Clipboard context feature in Syncfusion Code Studio to include recently copied content for enhanced AI interactions.
platform: syncfusion-code-studio
keywords: Syncfusion Code Studio, syncfusion, clipboard, context, code-studio, developer-tools, AI, productivity
---
 
# Clipboard
 
The Clipboard context option in the Syncfusion Code Studio enables users to easily incorporate recently copied content from editor files into their AI conversations, improving context and productivity.
 
## How to use the Clipboard context
 
### 1. Open the Syncfusion Code Studio
 
In the Syncfusion Code Studio, the chat interface is located on the left-hand side. This is where you can interact with AI and ask questions or get assistance.

<img src="../../feature-images/open_chat.png" alt="open chat" />

 
### 2. Select Clipboard context
 
In the chat window, click the `@` button.
> **Note:** If you cannot locate the Clipboard context option in the list, you will need to add it manually to include this context provider in the config.yaml file. Please follow the steps outlined in this [link](/code-studio/features/context-providers/add-more-contextproviders/How-to-configure-more-contextproviders) to do so.


<img src="../../feature-images/click-context.png" alt="Clickcontext" />


Select clipboard from the list of context providers.
 
It will show recently copied clipboard contents one by one into your conversation.


<img src="../../feature-images/clipboardselect.png" alt="Clipboard opencontext" />


Select the necessary copied content you need from the copied clipboard contents list.  
> **Note:** Once you close the Syncfusion Code Studio  and reopen again the copied contents will not show again.  

<img src="../../feature-images/clipboardcontentselect.png" alt="Clipboard choose" />
 
### 3. Use Clipboard context with query
 
After selecting the copied content, input relevant details about the copied content in the chat window and click Enter. You will get the results.

<img src="../../feature-images/clipboardresult.png" alt="Clipboard output" />