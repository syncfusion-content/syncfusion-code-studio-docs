---
title: .sfcodeignore
Description: Instructions to specify files and directories to ignore during indexing in Syncfusion Code Studio.
platform: syncfusion-code-studio
keywords: sfcodeignore, ignore, indexing
---

# .Sfcodeignore

## Purpose

The “.sfcodeignore” file allows you to specify files or directories from your workspace that should be ignored during indexing when using the Syncfusion Code Studio. This is useful for excluding irrelevant, sensitive, or unnecessary files from being processed.

## When to Use
- You want to exclude irrelevant or sensitive files and folders from Code Studio indexing so they don’t appear in context providers or influence AI answers.


## Prerequisites
- Syncfusion Code Studio open with a workspace

## Steps

### 1.Create ".sfcodeignore" file 
- create ".sfcodeignore" file in your workspace and open it

<img src="../reference-images/ignore1.png" alt=".sfcodeignore">

### 2.Add a file/folder 
- Add the required files and folders in ".sfcodeignore" file to ignore while indexing.

**ADD PATTERNS**:
- Lines starting with # are comments.
- Trailing slash / matches only directories (dist/).
- Leading slash / anchors to repo root (/build/).
- Use ! to negate a previous ignore (re-include). 

**Examples**:
- node_modules/ # ignore folder
- *.log # all .log files
- /secrets/*.json # only under repo root
- docs/**/*.png # images anywhere under docs
- !docs/keep.png # re-include a specific file


<img src="../reference-images/ignore2.png" alt=".sfcodeignore">

### 3.Added files will be ignored
- After adding the required file/folders reload the Code Studio and the added files and folders will be ignored during indexing. 
- You can check this by using the file and folder context providers. Type '@' and open file and folder context providers. The added files and folders will not appear.

<img src="../reference-images/ignore3.gif" alt=".sfcodeignore">


## Validation
- After reloading, open @Files/@Folder: ignored paths should not appear.
- Temporarily remove a file in sfcodeignore file , reload, and confirm the path reappears.


## Troubleshooting
- **Files/folders seems not ignored**: ensure you have reloaded the Code Studio.
- Ensure the added patterns are correct.

