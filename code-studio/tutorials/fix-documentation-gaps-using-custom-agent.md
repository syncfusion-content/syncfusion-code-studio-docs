---
title: Fixing Documentation Gaps – Generate Accurate Developer Docs with AI
description: Learn how to use a custom Codebase Documenter agent in Syncfusion Code Studio to generate clear, beginner-friendly documentation for any codebase.
platform: syncfusion-code-studio
keywords: documentation, custom-agent, codebase-docs, ai-documentation, code-studio, knowledge-sharing
---

# Fixing Documentation Gaps: Generate Accurate Developer Docs with a Custom Agent

## Overview

Many teams have at least one project that nobody wants to touch because **the code is complex and the documentation is out of date—or missing entirely**. This tutorial shows you how to use a **Codebase Documenter** custom agent in Syncfusion Code Studio to turn that kind of codebase into clear, beginner-friendly documentation.

Instead of manually writing long README files and architecture notes, you will:

- Create (or reuse) a **Codebase Documenter** agent.
- Point it at your project.
- Let it analyze your code and generate tutorials and overviews automatically.

By the end, you will have a **repeatable workflow** to keep your documentation fresh without turning developers into full-time writers.

## Prerequisites

Before you start, make sure:

- **Syncfusion Code Studio is installed and configured.**  
  If not, follow Install and Configure: [Install and Configuration](/code-studio/getting-started/install-and-configuration)
- **You have a project folder opened in Code Studio** that you want to document.
- **You are familiar with Custom Agents in Code Studio.**  
  A *Custom Agent* is an AI assistant whose behavior you define using an `.agent.md` file inside your project’s `.codestudio/agents` folder. For details, see [Custom Agents](/code-studio/reference/configure-properties/custom-agents).

> Tip: For your first run, choose a project that is representative but not the largest monolith in your organization. This keeps the first documentation run fast and easy to review.

## What You Will Learn

By the end of this tutorial, you will be able to:

- Create or reuse a **Codebase Documenter** custom agent based on a `.agent.md` template.
- Point the agent at a local project and let it analyze your codebase.
- Generate beginner-friendly documentation including high-level overviews, architecture descriptions, and step-by-step tutorial “chapters”.
- Iterate safely using **Agent mode** and **checkpoints** so you can review and refine the output.
- Establish a **repeatable workflow** to keep your documentation in sync with code changes over time.

## Step 1: Create the Codebase Documenter Agent File

In this step, you will create the configuration file that turns a generic model into a documentation-focused **Codebase Documenter** agent.

1. **Open your project in Code Studio.**
2. **Create the agent configuration folder (if it does not exist):**
   - In the Explorer, create a folder named `.codestudio` at the root of your project.
   - Inside it, create a subfolder named `agents`.
   - Final path: `.codestudio/agents/`.
3. **Download or copy the agent template:**
   - Get the `Codebase Documenter` agent template from your team’s repository or from your shared templates location.  
   - The file should be named something like: `Codebase-Documenter.agent.md`.
   - If you maintain a GitHub template, link it clearly here, for example: [Download Codebase Documenter agent template](https://github.com/syncfusion/code-studio-agent-library.git).
  - For this tutorial, we used the example project [ej2-showcase-react-loan-calculator](https://github.com/syncfusion/ej2-showcase-react-loan-calculator.git).
4. **Place the template in your project:**
   - Copy `Codebase-Documenter.agent.md` into the `.codestudio/agents/` folder.
5. **Open the agent file in the editor:**
   - In the Explorer, expand `.codestudio/agents/`.
   - Select `Codebase-Documenter.agent.md` to open it.

You now have a documentation-focused agent configuration file attached to your project.

![Explorer showing the .codestudio/agents folder with the Codebase-Documenter.agent.md file](./tutorials-images/fix-docs-agent-setup.png "Set up the Codebase Documenter agent file in the .codestudio/agents folder")

> Note: A `.agent.md` file describes how the agent should behave—its name, description, tools, and detailed workflow. The example you provided (with stages for analyzing the repo and writing chapters) is a good starting point for this file.

## Step 2: Customize the Codebase Documenter Agent (Optional but Recommended)

Next, you can tune the agent so it matches your project and documentation style.

1. **Review the top metadata block** in `Codebase-Documenter.agent.md`:
   - Confirm or update:
     - `description` – for example, “Transform any codebase into beginner-friendly documentation and tutorials”.
     - `name` – for example, “Codebase Documenter”.
     - `argument-hint` – explain what inputs the agent expects (for example, “Specify a GitHub URL, local directory path, or ask to document the current workspace”).
2. **Confirm the model and tools:**
   - Ensure the `model` is set to your preferred model in Code Studio.
   - Check that the required tools for reading files, searching the codebase, and creating docs are listed (for example, `read/readFile`, `search/fileSearch`, `edit/createFile`).
3. **Skim the workflow instructions inside the file:**
   - Make sure they:
     - Emphasize beginner-friendly explanations.
     - Limit code examples to short, well-commented snippets.
     - Describe how to structure chapters and the main `index.md`.
4. **Adjust any project-specific details:**
   - If your repository is very large, you can:
     - Limit which folders to scan (for example, `src/`, `apps/api/`).
     - Exclude test, build, or asset directories.
   - If your team has naming conventions for docs (for example, `docs/architecture/`), update the instructions so the agent writes output to those folders.

> Tip: Think of this file as the “job description” for your documentation agent. The clearer it is, the better your generated docs will be.

## Step 3: Activate the Codebase Documenter Agent in Chat

Now that the agent is defined in your project, you can start using it from the Chat panel.

1. **Open the Chat view in Code Studio.**
2. **Select the Codebase Documenter agent:**
   - Click the **agent dropdown** at the top of the chat panel.
   - Choose **Codebase Documenter** from the list.
3. **Confirm the agent is active:**
   - The agent’s description should appear as a hint or subtitle in the chat input area.
   - You should see that you are now chatting with **Codebase Documenter**, not the default agent.

> Note: If you do not see the agent in the dropdown, double-check that:
> - The `.agent.md` file is inside `.codestudio/agents/`.
> - The file name ends with `.agent.md`.
> - There are no syntax errors in the metadata block at the top.

> For a deeper understanding of Agent behavior, see [Agent](/code-studio/features/agent).

![Chat view showing Codebase Documenter selected in the agent dropdown](./tutorials-images/fix-docs-agent-select.png "Select the Codebase Documenter agent in Chat")

## Step 4: Ask the Agent to Document Your Codebase

With the agent selected, you can now ask it to analyze your project and generate documentation.

1. **Choose your scope:**
   - If your project is already open in Code Studio and you want docs for everything, you can target the **current workspace**.
   - If you want to focus on a subfolder (for example, `src/`), mention that explicitly in your request.
2. **Send a focused initial request in Chat, for example:**
   ```
   Document the current workspace. Identify core components, explain how they work together, and generate beginner-friendly tutorials.
   ```
3. **Let the agent run:**
   - The agent will typically:
     - Scan relevant folders and important source files.
     - Identify core abstractions (services, controllers, widgets, modules, and so on).
     - Map out how those pieces relate to each other.
     - Generate:
       - An `index.md` file with a high-level overview and table of contents.
       - A series of chapter files (for example, `01_overview.md`, `02_authentication.md`, and so on).
4. **Watch the tool usage and status messages** in the chat:
   - You should see the agent:
     - Listing files.
     - Reading source code.
     - Creating new Markdown files in an output folder.

![Chat session showing the Codebase Documenter agent scanning files and creating documentation](./tutorials-images/fix-docs-agent-run.png "Codebase Documenter generating documentation")

At this point, you have offloaded the hardest part of documentation: **understanding and organizing the code**.

## Step 5: Review and Refine the Generated Documentation

AI-generated documentation is a draft. You stay in control of quality and correctness.

1. **Open the generated docs in the Explorer:**
   - Look for an output folder created by the agent, for example: `output/my-project/`.
   - You should see:
     - `index.md` – overview and architecture.
     - Several chapter files – individual topics.
2. **Start with `index.md`:**
   - Check:
     - Does the project summary sound correct?
     - Does the architecture diagram (if any) match reality?
     - Does the table of contents reflect how you want newcomers to learn the system?
3. **Skim through a few chapter files:**
   - Do the chapter titles match major areas of your architecture?
   - Are explanations accurate enough for a new teammate?
   - Are code examples short enough to read quickly and correct in terms of APIs and behavior?
4. **Give targeted feedback through follow-up prompts:**
   - If something is unclear or wrong, go back to Chat and say, for example:
     ```
     The data flow section is confusing. Please rewrite Chapter 3 with a clearer sequence diagram and shorter explanations.
     ```
   - Or:
     ```
     Chapter 2 over-explains basic React concepts. Focus more on how our custom hooks work and less on React fundamentals.
     ```
5. **Let the agent regenerate or refine specific chapters** instead of rewriting everything by hand.

> Tip: Treat the AI as a **junior technical writer**. The agent writes first drafts; you review, correct, and approve. This keeps you in control while still saving time.

![Explorer showing generated index.md and chapter files inside an output folder](./tutorials-images/fix-docs-output-folder.png "Generated documentation files from the Codebase Documenter")

## Step 6: Keep Documentation in Sync with Code Changes

Documentation is only useful if it stays up to date. With a dedicated documentation agent, keeping docs current becomes a quick habit instead of a big project.

Here is a simple workflow you can adopt:

- **After each major feature or refactor:**
  - In Chat, ask the agent:
    ```
    Compare the current workspace with the last documented version and update any sections that are now outdated.
    ```
  - The agent can:
    - Re-scan key modules.
    - Update specific chapters.
    - Flag places where behavior seems to have changed.

- **When onboarding a new area of the codebase:**
  - Ask for a **focused tutorial** on that area, for example:
    ```
    Create a beginner-friendly tutorial for the billing module under src/billing.
    ```

- **During or after code review:**
  - If a change is unclear, ask the agent to:
    ```
    Explain how the new checkout flow works based on the code in src/checkout. Summarize the main steps and data flow.
    ```
  - Paste the explanation into your documentation (or have the agent write directly into a chapter file).

To keep your workspace safe while the agent reads and writes documentation files, you can combine this workflow with **Agent mode** and **checkpoints**:

- **Agent mode** gives the agent controlled access to your workspace.
- **Checkpoints** capture snapshots of your workspace so you can revert if needed.

Learn more:

- [Agent](/code-studio/features/agent)
- [Checkpoints](/code-studio/features/checkpoints)

## Verification

Use this checklist to verify that your AI-generated documentation is useful and working as intended:

- **Agent is available**
  - The `Codebase Documenter` agent appears in the Chat agent dropdown.
  - Its description matches the purpose of creating beginner-friendly documentation.

- **Docs were generated**
  - An output folder exists in your workspace (for example, `output/my-project/`).
  - The folder contains:
    - `index.md` – main overview.
    - One or more chapter files (for example, `01_overview.md`, `02_authentication.md`, and so on).

- **Content matches reality**
  - Core components, data flows, and responsibilities are described correctly.
  - Major architectural decisions are accurately reflected.
  - Code examples compile (or are easy to adjust so they do).

- **New developers can follow it**
  - Ask a teammate (or a junior developer) to:
    - Read `index.md` and one or two key chapters.
    - Answer questions like “Where is the authentication logic implemented?” or “Where do we send email notifications?”.
  - If they can find the answers quickly, your docs are doing their job.

If any of these checks fail:

- Refine the agent instructions in `Codebase-Documenter.agent.md`.
- Use more specific prompts in Chat.
- Regenerate only the sections that need improvement instead of starting from scratch.

## What’s Next?

You now have a **repeatable way to close documentation gaps** using AI, without turning engineers into full-time writers.

Here are some ideas for your next steps:

- **Build a review pipeline**
  - Add a handoff from your `Codebase Documenter` agent to a dedicated **Review** agent that checks documentation for accuracy and tone and flags sections that may be out of sync with the latest code.

- **Create project-specific variants**
  - For example:
    - `Mobile App Documenter` for mobile repositories.
    - `Backend API Documenter` for service-oriented backends.
  - Each variant can:
    - Focus on different folders.
    - Use different examples and diagrams.

- **Integrate with your existing Custom Agents**
  - Combine the Codebase Documenter with:
    - Custom QA agents for validation.
    - Architecture advisors.
    - Onboarding agents that answer “How does X work?” questions for new hires.

- **Explore related guides and references**
  - Custom Agents reference: [Custom Agents](/code-studio/reference/configure-properties/custom-agents)
  - General agent behavior and options: [Agent](/code-studio/features/agent)

With the right custom agent in place, your codebase stops being a mystery and becomes a **living, teachable system**—for you, your teammates, and every new developer who joins later.
