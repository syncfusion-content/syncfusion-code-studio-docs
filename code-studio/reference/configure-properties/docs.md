---
title: docs
description: Details about configuring documentation sources to be indexed and made available for Syncfusion Code Studio IDE's language models.
platform: syncfusion-code-studio
control: IDE
documentation: Getting Started
keywords: code, IDE, installation, windows, setup, getting-started
---

# Docs

## Purpose
The "Docs" section in Code Studio allows you to integrate documents directly into the environment. This means Code Studio can access and utilize these documents at any time, enhancing its ability to provide relevant assistance based on your specific information.

## When to Use
- You want the assistant to answer using specific external documentation (framework guides, API refs) without pasting text. 
- You need focused, doc-aware help tied to chosen pages rather than the whole web. You prefer tight scope control and predictable performance.


## Prerequisites
- Syncfusion Code Studio open with a workspace
- Documentation site link to integrate


## Steps

### 1. Navigate to the "Docs" Section
In Code Studio, locate and click on the "Docs" section.

### 2. Initiate Document Addition
Within the "Docs" section, you will find an option labeled "Add Docs". Click on this button.

<img src="../reference-images/adddocs.png" alt="Image of added documents list">

### 3. Enter Document Details
A new window will appear. Give the title and url for the document.

**Title:** Enter a descriptive title for your document. This title will help you easily identify the document in the list.

**URL:** Provide the URL to your document.

<img src="../reference-images/docs1.png" alt="Image of added documents list">

### 4. Confirm Addition
Click on the "Add" button to finalize the process. Your document will now be integrated into Code Studio.

<img src="../reference-images/docs.png" alt="Image of added documents list">

### 5.Managing Your Added Documents
Once documents are added, they will be listed in the "Docs" section.

<img src="../reference-images/docslist.png" alt="Image of added documents list">

### 6.Editing Document Details
To modify the title or URL of an existing document,
Click on the "Edit" option next to the desired document in the list.
This action will open the configuration file.
You can then edit the name and URL directly within the config page.

<img src="../reference-images/docsedit.png" alt="Image of added documents list">

**Note:** To access the added documents refer the steps in this [page](/code-studio/features/context-providers/docs).

## Validation
- Add one doc page and ask for a summary; confirm the answer cites concepts from that page. 
- Add a second page and ask for a code sample; verify details come from both.


## Troubleshooting
- **Page not indexing or slow**: check network; try a smaller page or wait for indexing to complete. 
- **Response Too slow/expensive**: reduce the number of URLs or pick shorter pages; avoid whole-site imports.

