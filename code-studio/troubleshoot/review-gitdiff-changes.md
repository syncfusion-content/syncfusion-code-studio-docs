---
title: Review Git Diff Changes
description: Guide on reviewing Git diff changes in Syncfusion Code Studio.
platform: syncfusion-code-studio
keywords: git diff, review changes, code studio, version control, ai assistance, code modifications
---

# Review Git Diff Changes in Code Studio

## Problem Summary

Previously, users could view git diff / uncommitted changes in Code Studio by typing **@Git Diff** in the chat box or by using the **"Add context"** button and selecting the git diff option. In the current version, this functionality has been moved and is now accessed by typing **#** in the chat input box and selecting **#changes** from the dropdown menu.


## Resolution Steps

### Steps to Use #changes

1. Make sure the desired project/workspace is open and active in Code Studio — preferably one that is connected to a GitHub repository. The **#changes** tool only shows modifications from the currently opened project.

2. Go to the chat panel in Code Studio where you interact with the AI assistant.

3. In the chat input box type #, a dropdown menu will appear showing available options. From this dropdown, select #changes.

<img src="./troubleshoot-images/changes_tool_drop_down.png" alt="trouble shoot"  />

4. After selecting #changes, type your specific question or request regarding the current changes.

5. Send the prompt and the response will include the current git diff information, typically shown file-by-file with added/removed lines highlighted.

<img src="./troubleshoot-images/git_diff_response.png" alt="trouble shoot"  />

## Best Practices

- Write clear and specific questions so the #changes tool can focus on exactly what you want to see.
- Keep your question focused and ask about one area, file, or type of change at a time.
- Review the diff carefully before staging, committing, or merging changes, especially when many files are modified.
- Refine your question or ask a follow-up if you need a shorter summary, more explanation, or only certain types of changes.