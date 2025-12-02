---
title: Setup and Debug Desktop Applications in Syncfusion Code Studio
description: Step-by-step guide to setup and debug Desktop applications using Syncfusion Code Studio's debugging features and tools.
platform: syncfusion-code-studio
control: IDE
documentation: Troubleshoot
keywords: winforms, wpf, winui, wf, desktop-applications, debug, debugging, breakpoints
---

# This Guide provides Step-By-Step Instructions for Setting-Up and Debugging a Desktop Application using Code Studio

## Prerequisites

- Install the .NET SDK (version 8.0 or 9.0, depending on your project requirements) from [dotnet-sdk](https://dotnet.microsoft.com/en-us/download)
- Install the Windows App SDK (version 1.8.x) from [windows-app-sdk](https://learn.microsoft.com/en-us/windows/apps/windows-app-sdk/downloads) (Required only for WinUI applications)

## Pre-Installed Extensions of Code Studio

Refer this page to know more about [Pre-Installed Extensions of Code Studio](../../pre-installed-extensions)


## Steps to Setup a Desktop Application in Code Studio

### Step 1: Create a Solution
Navigate to the solution and create a new solution.

<img src="desktop-images/create-solution.png" alt="createsolution">

### Add a Project to the Solution:

Step 1: Include the new project in the solution.
<img src="desktop-images/new-project.png" alt="newproject">

Step 2:

**WinForms** - Create a WinForms project by selecting the WinForms template

<img src="desktop-images/winforms-template.png" alt="winformstemplate">

**WPF** - Create a WPF project by selecting the WPF template

<img src="desktop-images/wpf-template.png" alt="wpftemplate">

**WinUI** - Create a WinUI project by selecting the WPF template

<img src="desktop-images/winui-template.png" alt="winuitemplate">

Step 3: Specify the Programming language (Skip this step for WinUI  )

<img src="desktop-images/select-language.png" alt="selectlanguage">

Step 4: Specify the Project Name

<img src="desktop-images/create-project.png" alt="createproject">

Step 5: Specify the Folder Name

<img src="desktop-images/create-folder.png" alt="createfolder">


New Project will be created in the solution

**Winforms**

<img src="desktop-images/winforms-setup.png" alt="winformssetup"> 

**WPF**

<img src="desktop-images/wpf-setup.png" alt="wpfsetup">

**WinUI**

<img src="desktop-images/winui-setup.png" alt="winuisetup">


### Set Up Tasks for Building:

Create a launch.json file to configure the build process

<img src="desktop-images/create-json.png" alt="createjson">

Select .NET Core Debugger

<img src="desktop-images/select-debugger.png" alt="selectdebugger">

### Build the Project

<img src="desktop-images/build-project.png" alt="buildproject">

### Run the Application

Go to "Run and Debug"and select ".NET Core Debugger (launch)"

<img src="desktop-images/run-app.png" alt="runapp">


## Debugging in Action & Features

The Debugging in Action walkthrough and the complete debugging feature reference have been moved to the [Debugging Steps Reference](debugging-steps). Please refer to that page for:

- Platform-independent debugging workflows
- Debugging keyboard shortcuts
- Feature tables and descriptions for all supported desktop UI frameworks

This ensures that you always have a single, up-to-date reference for all debugging actions in WinForms, WPF, and WinUI projects.