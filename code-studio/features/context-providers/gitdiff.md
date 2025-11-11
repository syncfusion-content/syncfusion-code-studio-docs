---
title: Using the Git Diff Context in Syncfusion Code Studio
description: Learn how to use the GitDiff context feature to summarize, review, and verify changes made in your Git branch using Syncfusion Code Studio.
platform: syncfusion-code-studio
keywords: code, syncfusion, git-diff, context, ai-assistance, developer-tools, commit-review, code-summary
---

# Git Diff

## Purpose
The Git Diff Context provider lets you reference all changes made in your current branch to get a summary of your work or request a general review. This is especially useful for reviewing progress, identifying improvements, or preparing for a commit by ensuring the modifications align with project goals and coding standards.

## When to Use
- You want the assistant to analyze and summarize all the code changes made in your current Git branch.  
- You need help preparing a commit, reviewing your changes, generating release notes, or ensuring code modifications align with project goals and standards.

## Prerequisites
- Syncfusion Code Studio open with a project.  
- GitDiff Context provider available in the @ menu.  
- Git branch with code changes.

## Steps

### 1. Select GitDiff Context
- In the Code Studio chat window, click the @ button. A menu will appear—select GitDiff.
> **Note:** If you cannot locate the GitDiff context option in the list, you will need to add it manually by including this context provider in the config.yaml file. Please follow the steps outlined in this [link](/code-studio/features/context-providers/add-more-contextproviders/how-to-configure-more-contextproviders) to do so.


### 2. Use GitDiff Context with Query
- Git Diff Context allows you to programmatically gather and reference all code changes made in your current Git branch. It is especially helpful when you want to:  
  - Summarize your work before creating a commit or pull request  
  - Request a review of recent modifications  
  - Generate AI-assisted documentation, commit messages, or release notes  
  - Verify the scope and impact of changes to ensure they align with the intended feature or fix
- Large diffs or many files may increase analysis time and token usage.  
- Narrow scope as needed to ensure quicker feedback and concise reviews.

<img src="../feature-images/gitdiffcontext.gif" alt="gitdiff" />

## Validation
- Make several changes in your branch, then select @GitDiff and ask for a summary; confirm the assistant lists main updates clearly.  
- Use @GitDiff on a single file and ask for a quality or standards review; verify the feedback references actual changes.

## Troubleshooting
- **Feedback feels generic**: narrow the diff scope to specific files or include a targeted question (file, feature, or issue).  
- **No related responses**: ensure your workspace folder is a valid Git repository.
