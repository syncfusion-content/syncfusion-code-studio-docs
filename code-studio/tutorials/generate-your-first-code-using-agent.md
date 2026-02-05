---
title: Generate Your First Code Change Using Agent
description: Learn how to use Agent mode in Syncfusion Code Studio to generate, review, and manage code changes with AI assistance.
platform: syncfusion-code-studio
keywords: agent-mode, ai-coding, code-generation, code-review, checkpoints
---

# Generate Your First Code Change Using Agent

This tutorial guides you through using Agent mode in Syncfusion Code Studio. Agent mode enables autonomous AI-powered coding capabilities, allowing you to generate, review, and manage code changes with AI assistance. You will learn how to enable Agent mode, instruct the AI with prompts, review proposed changes, and utilize checkpoints to manage code iterations. For more information about Agent mode, see [Agent](/code-studio/features/agent).

## Prerequisites

Before beginning, ensure:

- Syncfusion Code Studio is installed and properly configured on your system. If you have not yet downloaded Code Studio, refer to [Install and Configure](/code-studio/getting-started/install-and-configuration.md) for step-by-step instructions.
- Your project is opened in Code Studio, or you have at least one folder open.

## What You Will Learn

By the end of this tutorial, you will be able to:

- Enable Agent mode within Code Studio.
- Use prompts to initiate AI-assisted code changes.
- Review and evaluate suggested code modifications using side-by-side comparison.
- Accept or reject proposed changes using Keep or Undo options.
- Understand detailed summaries of all changes made.
- Manage project states and restore previous versions using checkpoints.

## Steps to Generate Code

### Step 1: Enable Agent Mode

1. Open Syncfusion Code Studio with your target project or a new folder.
2. Click the mode selector in the interface.
3. Select **Agent Mode** from the dropdown menu. Agent Mode enables autonomous coding capabilities, allowing the AI to analyze, edit, and manage your codebase.
4. Confirm that Agent Mode is active by checking for the tick mark status indicator in the interface.

   <img src="./tutorials-images/firstagentchange1.png" alt="Enable Agent Mode" />

### Step 2: Describe Your Task

1. In the chat input field, enter your coding request or task description.

   >**Tip:** Be as specific as possible with your instructions to achieve better results.

2. Press **Enter** to submit your request.
3. The Agent will:
   - Analyze and understand your request.
   - Explore the relevant codebase sections.
   - Use appropriate tools to make changes.
   - Suggest necessary code modifications.

   <img src="./tutorials-images/firstagentchange2.png" alt="Agent processing request" />

### Step 3: Review the Proposed Changes

1. The Agent displays a side-by-side comparison of all proposed modifications.
2. Examine each change carefully to ensure it aligns with your intent.
3. For each change, use the options provided in the chat:
   - Click **Keep** to approve and apply the change.
   - Click **Undo** to reject and discard the change.

   <img src="./tutorials-images/firstagentchange3.png" alt="Review changes" />

### Step 4: Review the Code Change Summary

1. Once all changes are complete, the Agent provides a detailed summary.
2. The summary lists:
   - All files modified.
   - New files created.
   - Tools used during the process.
3. Review this summary carefully to confirm all changes match your requirements.

### Step 5: Manage Using Checkpoints

1. The Agent automatically creates checkpoints between chat requests.
2. Checkpoints provide a safety net by allowing you to:
   - Review changes at different stages.
   - Restore your code to any previous checkpoint if needed.

   <img src="./tutorials-images/firstagentchange4.png" alt="Checkpoints" />

## Verification

To confirm everything worked as expected:

- **Agent Mode:** Verify that Agent Mode is active and you have granted all necessary tool permissions.
- **Changes Applied:** Review your codebase and confirm that all accepted changes have taken effect.
- **Summary Accuracy:** Check the final summary to ensure all intended files were modified or created as described.
- **Checkpoints:** Locate the available checkpoints (usually visible at the bottom of each chat request) and attempt to restore one to confirm the feature works correctly.
- **Permissions:** If tool calls are not executing, verify that you have granted permission for tool access in the settings.

For more details about checkpoints, see [Checkpoints](/code-studio/features/checkpoints).

## Next Steps

Now that you have successfully generated your first code change using Agent mode:

- Learn about **checkpoint** to efficiently manage your project versions. See [Checkpoints](/code-studio/features/checkpoints) for details.
- Review the **Agent mode features** guide for additional capabilities. See [Agent](/code-studio/features/agent) for details.
