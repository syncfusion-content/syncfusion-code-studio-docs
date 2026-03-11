---
title: Generate Web Automation Tests Using Playwright MCP
description: Learn how to use Playwright MCP with Agent mode in Syncfusion Code Studio to generate, execute, and manage web automation tests with AI assistance.
platform: syncfusion-code-studio
keywords: playwright-mcp, agent-mode, web-automation, ai-testing, mcp-server
---

# Generate Web Automation Tests Using Playwright MCP

## Overview 

Ready to transform your web testing workflow? In this tutorial, we'll explore Playwright MCP with Code Studio's Agent mode. Imagine having an AI teammate that understands your testing requirements, generates Playwright test scripts, executes them in real-time, and shows you comprehensive test reports—all within your development environment. That's what Playwright MCP with Agent mode delivers!

### What is an MCP Server?

The Model Context Protocol (MCP) server is a specialized bridge that connects AI agents with external tools and services. It enables the AI to perform real-world actions—like running tests, accessing databases, or automating browser tasks—rather than just generating code suggestions. In this tutorial, the MCP server orchestrates Playwright to execute actual browser automation tasks based on your instructions.

### What is Playwright MCP Server?

The Playwright MCP Server is a specific implementation that brings Playwright's powerful browser automation capabilities to AI agents. It acts as a translator between natural language commands and browser actions. When you tell the AI to "verify the login button exists," the Playwright MCP Server converts this into executable Playwright code that actually navigates pages, clicks elements, fills forms, and captures results. This integration makes AI-powered test generation not just possible, but remarkably efficient.

By the end of this tutorial, you'll be comfortable using Playwright MCP with Agent mode to create end-to-end tests without manually writing code. Let's get started!

For deeper understanding of Agent mode capabilities, check out [Agent](/code-studio/features/agent).

## Prerequisites

Before beginning, ensure:

- Syncfusion Code Studio is installed and properly configured on your system. If you have not yet downloaded Code Studio, refer to [Install and Configure](/code-studio/getting-started/install-and-configuration) for step-by-step instructions.
- Node.js (v18 or higher) is installed. Playwright requires Node.js to run automation tests. Download from [nodejs.org](https://nodejs.org/) and verify installation with `node --version`.
- Your project is opened in Code Studio, or you have at least one folder open.

## What You Will Learn

By the end of this tutorial, you'll be able to:

- Install and configure Playwright MCP server in Code Studio
- Enable Agent mode for AI-powered test generation
- Create test scenarios in natural language and watch AI generate executable test scripts
- Review and execute generated Playwright tests

## Steps to Generate Playwright Tests

### Step 1: Install Playwright and MCP Server

Let's set up Playwright and connect it with the MCP server in Code Studio.

1. Open Syncfusion Code Studio with your project folder or create a new empty folder.
2. Open the integrated terminal (**Terminal** → **New Terminal**).
3. Install Playwright by running the following command:

   ```bash
   npm init playwright@latest
   ```

4. Follow the installation prompts:
   - Press **Enter** to confirm installation
   - Select **TypeScript** as the language (default) and press **Enter**

    <img src="./tutorials-images/typescript-selection.png" alt="TypeScript Selection" />
   
   - Accept the default `tests` folder for end-to-end tests by pressing **Enter**
   
    <img src="./tutorials-images/test-folder-configuration.png" alt="Test folder configuration" />
    <br><br>
    <img src="./tutorials-images/test-folder-confirmation.png" alt="Test folder confirmation" />
   
   - Press **Enter** to continue with the setup
   - Confirm installation of Playwright browsers
    <img src="./tutorials-images/browser-installation.png" alt="Browser installation" />

   The installation will download browser binaries. Once complete, you'll see the Playwright folder structure in your project explorer.

    <img src="./tutorials-images/project-structure.png" alt="Playwright project structure" />

5. Install the Playwright MCP Server:
   
   - Click on the **MCP** icon in the Code Studio sidebar
      <img src="./tutorials-images/mcp-icon.png" alt="MCP icon" />
   - In the Code Studio marketplace, select the Playwright MCP tools
      <img src="./tutorials-images/mcp-marketplace.png" alt="MCP marketplace" />
   - Click on the **Install** icon and choose your installation option (global or local)
   <img src="./tutorials-images/installation-scope.png" alt="Installation scope" />
   - Click your option to add the Playwright MCP server to the installed tabs


6. Verify the MCP installation:
   - After installation, the Playwright MCP server will be connected
   - Verify the connection status shows as active/connected
      <img src="./tutorials-images/mcp-connection-active.png" alt="MCP installation" />
   - From the context menu options, select **Edit Configuration (JSON)**
      <img src="./tutorials-images/edit-configuration-menu.png" alt="Connection active" />
   - After installing Playwright MCP server, an MCP entry will be added to the configuration. The MCP server will be running by default. To stop it anytime, you can click on the **Stop** button
      <img src="./tutorials-images/mcp-server-running.png" alt="Connection confirmed" />

     - To verify the Playwright MCP server installation, click the **Select Tools** icon in the Code Studio chat panel. You should see "MCP server: playwright" listed with available Playwright commands
     
      <img src="./tutorials-images/available-tools.png" alt="Available tools" />


### Step 2: Create the Required Skills

Skills help guide the AI agent to perform specific tasks. Let's create a skill for Playwright test generation.

1. Open the Code Studio menu and click on **Skills**.

   <img src="./tutorials-images/skills-menu.png" alt="Skills menu option" />

2. Create a new skill:
   - Click **+ New skill...** from the skills panel
   
   <img src="./tutorials-images/create-new-skill.png" alt="Create new skill" />

3. Name your skill:
   - Enter `playwright-explore-website` as the skill name (use lowercase letters, numbers, and hyphens only)
   - Press **Enter** to confirm
   
   <img src="./tutorials-images/skill-name-input.png" alt="Name the skill" />

4. Define the skill instructions in the `SKILL.md` file:

   ```markdown
    ---
    name: playwright-explore-website
    description: 'Website exploration for testing using Playwright MCP'
    ---

    # Website Exploration for Testing

    Your goal is to explore the website and identify key functionalities.

    ## Specific Instructions

    1. Navigate to the provided URL using the Playwright MCP Server. If no URL is provided, ask the user to provide one.
    2. Identify and interact with 3-5 core features or user flows.
    3. Document the user interactions, relevant UI elements (and their locators), and the expected outcomes.
    4. Close the browser context upon completion.
    5. Provide a concise summary of your findings.
    6. Propose and generate test cases based on the exploration.
   ```
   
   <img src="./tutorials-images/skill-instructions.png" alt="Skill instructions defined" />


### Step 3: Enter Your Test Scenario and Run the Agent

1. Enable Agent Mode:
   - Click the mode selector in the Code Studio interface
   - Select **Agent Mode** from the dropdown menu

2. Select your skill:
   - In the chat panel, type `/` to open the skills
   - Choose `playwright-explore-website` from your available skills

3. Enter your test scenario in natural language:

   ```
    1. Navigate to "https://ej2.syncfusion.com/showcase/angular/appointmentplanner/#/dashboard".
    2.Verify that the page title contains "Appointment Planner" or "Example Clinic".
    3.Check that the header displays the logged-in user's name (e.g., "Jane Doe") and role (e.g., "Admin").
    4.Confirm the presence of the main navigation menu / sidebar with items like: Dashboard, Schedule, Doctors, Patients, Preference, About.
    5.Verify that the "Logout" button/link is visible in the header or sidebar.
    6.Check that clicking the "Dashboard" menu item (if visible) keeps/reloads the current view without errors.
   ```
    <img src="./tutorials-images/test-scenario-input.png" alt="Test scenario input" />

3. Press **Enter** to submit your request.
4. Watch the Agent work its magic. You'll see it:
   - Think about your request and understand what you're asking for
   - Use Playwright MCP tools to interact with the browser
   - Generate the test code
   - Execute the test to verify it works
   - Prepare results for you to review

    <img src="./tutorials-images/agent-execution.png" alt="Agent executing the test generation" />

### Step 4: Review the Generated Test

The Agent shows you the generated test and execution results.

1. Review the generated test file in the `tests/` folder (e.g., `appointment-planner-verification.spec.ts`):

  <img src="./tutorials-images/generated-test-file.png" alt="Generated test file" />

2. Check the terminal output showing test execution results.

   Check the Code Studio terminal for the execution details. By default, it runs headless on 3 workers: Chromium, Firefox, and WebKit.

  <img src="./tutorials-images/test-execution-terminal.png" alt="Test execution in terminal" />
  <br><br>
  <img src="./tutorials-images/test-results-summary.png" alt="Test results summary" />

3. View the HTML report by running:

   ```bash
   npx playwright show-report
   ```

  <img src="./tutorials-images/html-report-command.png" alt="Running the HTML report command" />
  <br><br>
  <img src="./tutorials-images/html-report-view.png" alt="HTML report view" />


## Verification

Let's make sure everything went smoothly! Here's your verification checklist:

- **Agent Mode is On?** Look at the mode selector—does it show "Agent Mode" is active?

- **Playwright and MCP Installed?** Check that `playwright.config.ts` exists in your project root and verify Playwright MCP server shows as connected in the MCP panel

- **Test Generated Successfully?** Open the `tests/` folder and confirm your test file exists. Check terminal output for test execution results showing passed tests

- **Test Report Accessible?** Run `npx playwright show-report` and verify the HTML report opens

Congratulations! You've just completed your first AI-generated web automation test. You've transitioned from manual test writing to AI-powered Playwright test generation!


## What's Next? Continue Your Learning Journey

You've mastered the basics, but there's so much more to explore:

- **Want to dive deeper into checkpoints?** Head to [Checkpoints](/code-studio/features/checkpoints) to learn how to manage multiple versions of your tests like a pro.

- **Curious about what else Agent mode can do?** Check out the [Agent](/code-studio/features/agent) feature guide for advanced tips and tricks.