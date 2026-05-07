---
title: Build Your First App Using Spec-Driven Development
description: "Learn how to build a Voice Notes web app using Spec-Driven Development (SDD) approach with Syncfusion Code Studio"
classification: "User Guide - Tutorial"
platform: syncfusion-code-studio
keywords: spec-driven-development, ai-development, voice-notes-app, openspec, code-generation, agent-mode
---

# Build Your First App Using Spec-Driven Development

## Overview

Building applications with AI can be unpredictable when instructions are unclear. **Spec-Driven Development (SDD)** solves this by defining exactly what you want to build before you start coding. This approach reduces guesswork and ensures your AI agent generates code that matches your vision.

In this beginner-friendly guide, you'll learn how to build a **Voice Notes web app** from scratch using the SDD approach in Code Studio. You'll go from idea to a working application by following a structured methodology that combines clear specifications, detailed planning, and AI-assisted code generation.

## Prerequisites

Before getting started, make sure that:

1. **Syncfusion Code Studio is installed**  
   If it’s not installed, refer to the [installation guide](/code-studio/getting-started/install-and-configuration) to set it up properly.

2.	Node.js >= 20.19.0 is installed.

## What You'll Learn

By the end of this tutorial, you'll know how to:
- Understand what Spec-Driven Development (SDD) is and why it matters for AI-powered development
- Understand what OpenSpec is and how it helps you build software predictably
- Set up your development environment and install OpenSpec
- Create a detailed project plan using the `/opsx:propose` command
- Review the generated proposal, design, specifications, and tasks
- Implement your plan using the `/opsx:apply` command to generate code
- Test and run your completed Voice Notes web application
- Finalize and organize your project using the `/opsx:archive` command

## Understanding SDD and OpenSpec

### What is Spec-Driven Development (SDD)?

Spec-Driven Development (SDD) is a methodology that emphasizes creating clear, structured specifications before writing any code. Instead of jumping straight into coding and hoping everything works out, you first write down exactly what you want to build, how it should behave, and what it should do.

**Why it matters:**
- **Reduces confusion** — Everyone (including AI) knows exactly what to build
- **Improves collaboration** — Your specifications become the shared source of truth
- **Better quality** — Clear requirements lead to fewer mistakes and less rework

Unlike traditional approaches where code often becomes the de-facto specification, SDD treats specifications as living documents. You write your requirements in plain English (using Markdown files), and then AI agents generate the implementation based on those specifications.

### What is OpenSpec?

OpenSpec is a structured workflow tool that helps you organize AI-powered development in a predictable way. Think of it as a project manager for working with AI to build software. Instead of letting AI make random changes, OpenSpec keeps everything organized and transparent.


For more information about open spec, visit our [Using OpenSpec in Code Studio](/code-studio/tutorials/using-openspec-inside-syncfusion-code) guide.

## Build Your First App in Code Studio

### Step 1: Set Up Your Environment

Before building your Voice Notes app, ensure your Code Studio environment is ready:


1. **Create a new workspace**:
   - Create a new folder named `voice-notes-app` on your machine
   - Open Code Studio on your machine
   - Select the new folder as your workspace in code studio by clicking **File** -> **Open Folder**

### Step 2: Install OpenSpec


1. **Open the Terminal** in Code Studio (`Terminal` → `New Terminal`)
2. **Install OpenSpec** by running this command:
   ```
   npm install -g @fission-ai/openspec@latest
   ```
3. **Initialize the spec structure** in your project folder:
   ```
   openspec init
   ```
   This creates a folder structure to organize your proposal, specification, and design documents.

   <img src="../gettingstarted-images/voiceapp1.png" alt="voice app" />

> **Tip**: If you have UI designs or wireframes for your Voice Notes app, add them to your project folder now. You can reference them later when defining specifications.

### Step 3: Create Your Change Plan (Propose)

**What happens in this step:**
You tell Code Studio's AI what you want to build by describing your Voice Notes app in detail. The AI reads your description and creates a complete project plan for you. This plan includes:
- A **proposal** explaining what you're building and why
- A **design** describing how it will work
- **Specifications** for each part of the app
- **Tasks** — a checklist of all the work needed

All of these are saved as markdown files you can read and edit.

**How to do it:**
Type the `/opsx:propose` command in the Code Studio Chat Panel. This command tells Code Studio to start the planning process. Follow it with a detailed description of what you want to build.

Example prompt:

```
/opsx-propose

Build a Voice Notes Web App with:

Features:
- Record voice → auto-transcribe to text (Web Speech API)
- Search notes by keywords, pin/edit/delete notes
- Optional AI enhancement (GPT-4.1 via OpenRouter)
- Settings: theme (Light/Dark/System), font size

Pages: Auth (signup/signin), Onboarding (4-slide carousel), Dashboard (search + note grid), Voice Recorder, Note Editor, Settings

Tech Stack:
- React 18 + TypeScript, Vite
- Syncfusion React Components
- SQLite (sql.js) + IndexedDB persistence
- Web Speech API (Chrome/Edge preferred)

Key Requirements:
- Client-side only, no backend/server
- Local-first storage in browser
- Auto-save after 2s inactivity
- Responsive: mobile-first (768px tablet, 1024px desktop)
- CRITICAL: Voice audio NOT stored, only transcribed text

Out of Scope v1:
- Cloud sync/backup, audio editing, multiple languages
- Export/import, sharing, advanced AI features
```

The AI will generate several markdown files in your `openspec/changes/` directory. Open the change folder to review the generated files:

**Understanding What Was Generated:**

The files you see represent OpenSpec's structured approach to planning changes:

- **Proposal** — A summary document describing what you want to build
- **Design** — Technical details about how it will be built
- **Tasks** — Step-by-step checklist of work to complete
- **Specs** — Detailed specifications for each file or component
- **Change folder** — The directory containing all these files for this specific change

Review these files carefully before proceeding to the next step. You can modify the markdown files directly if needed.

   <img src="../gettingstarted-images/voiceapp.gif" alt="voice app" />

### Step 4: Implement the Plan (Apply)

**What happens in this step:**
Now that your plan is ready, you tell the AI to start building. The AI reads all the specifications and tasks you approved in Step 3, then writes the actual code for your Voice Notes app. It works through the tasks one by one, creating files and writing code that matches your specifications exactly.

This is where your detailed plan from Step 3 becomes actual working code.

**How to do it:**
Type the `/opsx:apply` command in the Code Studio Chat Panel. This command tells the AI: "Start building based on my plan." The AI will then begin creating your application.

For example:

```
/opsx-apply
```

The AI will begin executing tasks one by one. You'll see progress updates in the chat as each task completes.

   <img src="../gettingstarted-images/voiceapp-apply.gif" alt="voice app" />

### Step 5: Run Your Application

Launching your completed app and verify it works end-to-end:

1. **Start the development server**:
   ```
   npm run dev
   ```

2. **Open your app** in a web browser (usually `http://localhost:3000`)

3. **Perform a full user walkthrough**:
   - Record and transcribe
   - Save and retrieve notes
   - Verify all features work smoothly

4. **Celebrate!** You've successfully built an app using Spec-Driven Development.

   <img src="../gettingstarted-images/voiceapp-final.png" alt="voice app" />

### Step 6: Finalize and Organize (Archive)

**What happens in this step:**
After building and testing your Voice Notes app, it's time to clean up and organize your project. The `/opsx:archive` command moves all your specifications to a main specs folder and archives your working files, keeping everything neat and organized. This is like filing away completed project documents so they don't clutter your workspace.

Archiving makes it easy to find your specifications later and prepares your project folder for the next feature you want to build.

**How to do it:**
Type the `/opsx-archive` command in the Code Studio Chat Panel. This command tells Code Studio: "Organize and finalize my work."

For example:

```
/opsx:archive
```

Check your project structure to verify the archiving worked correctly:

What you should see:

- Spec files moved to `openspec/specs/` (main specs folder)
- Change folder archived to `openspec/changes/archive/`
- Your project is now cleanly organized and ready for the next feature!

   <img src="../gettingstarted-images/voiceapp-archive.gif" alt="voice app" />


Congratulations! You've successfully built a Voice Notes web app using Spec-Driven Development approach. By following this workflow — planning with detailed specifications, implementing with AI assistance, and organizing your work — you've experienced how SDD makes AI-powered development predictable and maintainable. You can now use this same methodology to build other applications with confidence, knowing that clear specifications lead to better code and fewer surprises.
