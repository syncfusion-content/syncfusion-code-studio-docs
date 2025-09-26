---
title: Setup and Debug Desktop Applications in Syncfusion Code Studio
description: Step-by-step guide to setup and debug Desktop applications in WinForms, WPF and WinUI Platforms using Syncfusion Code Studio's debugging features and tools.
platform: syncfusion-code-studio
control: IDE
documentation: Troubleshoot
keywords: winforms, wpf, winui, wf, desktop-applications, debug, debugging, breakpoints, step-through, variables, watch, call-stack, output, troubleshoot, code-studio
---

# This guide provides step-by-step instructions for setting-up and debugging a Desktop application using Code Studio

## Prerequisites

- Install the .NET SDK (version 8.0 or 9.0, depending on your project requirements) from [dotnet-sdk](https://dotnet.microsoft.com/en-us/download)
- Install the Windows App SDK (version 1.8.x) from [windows-app-sdk](https://learn.microsoft.com/en-us/windows/apps/windows-app-sdk/downloads) (Required only for WinUI applications)

## Built-in Extensions of Code Studio
 - **DotRush** is a lightweight C# development environment for Visual Studio Code, enabling efficient .NET project management. It provides Roslyn-based IntelliSense for code completion and navigation, a solution explorer for handling multiple projects/solutions, integrated debugging (including .NET Core, Unity, and Godot), test exploration for running NUnit/xUnit tests, performance profiling tools, code decompilation, and multi-target diagnostics. Ideal for seamless .NET and game development on Windows, macOS, and Linux. For more details, visit: https://github.com/JaneySprings/DotRush
 
- **vscode-solution-explorer** is a Visual Studio Code extension that adds a Solution Explorer panel for managing .sln file, mimicking Visual Studio's structure. It is designed for .NET Core projects. For more details, visit: https://github.com/fernandoescolar/vscode-solution-explorer

<img src="debugging-images/extensions.png" alt="extensions">


## Steps to Setup a Desktop Application in Code Studio

### Step 1: Create a Solution
Navigate to the solution and create a new solution.

<img src="debugging-images/create-solution.png" alt="createsolution">

### Add a Project to the Solution:

Step 1: Include the new project in the solution.
<img src="debugging-images/new-project.png" alt="newproject">

Step 2:

**WinForms** - Create a WinForms project by selecting the WinForms template

<img src="debugging-images/winforms-template.png" alt="winformstemplate">

**WPF** - Create a WPF project by selecting the WPF template

<img src="debugging-images/wpf-template.png" alt="wpftemplate">

**WinUI** - Create a WinUI project by selecting the WPF template

<img src="debugging-images/winui-template.png" alt="winuitemplate">

Step 2A: Specify the Programming language (For WinForms and WPF)

<img src="debugging-images/select-language.png" alt="selectlanguage">

Step 3: Specify the Project Name

<img src="debugging-images/create-project.png" alt="createproject">

Step 3: Specify the Folder Name

<img src="debugging-images/create-folder.png" alt="createfolder">


New Project will be created in the solution

**Winforms**

<img src="debugging-images/winforms-setup.png" alt="winformssetup"> 

**WPF**

<img src="debugging-images/wpf-setup.png" alt="wpfsetup">

**WinUI**

<img src="debugging-images/winui-setup.png" alt="winuisetup">


### Set Up Tasks for Building:

Create a launch.json file to configure the build process

<img src="debugging-images/create-json.png" alt="createjson">

Select .NET Core Debugger

<img src="debugging-images/select-debugger.png" alt="selectdebugger">

### Build the Project

<img src="debugging-images/build-project.png" alt="buildproject">

### Run the Application

Go to "Run and Debug"and select ".NET Core Debugger (launch)"

<img src="debugging-images/run-app.png" alt="runapp">

## Debugging in Action

**Note:** The following debugging demonstration uses a WPF application, but the debugging process, interface, and features are identical across WinForms, WPF, and WinUI platforms in Syncfusion Code Studio.

### Debug Process Walkthrough

<img src="debugging-images/debug-app.gif" alt="Debug Process Demonstration">

The above animation demonstrates the complete debugging workflow from setting breakpoints to hitting them during execution.

The application will launch, and the debugger will attach. If a breakpoint is hit, execution pauses, and you can inspect variables in the Debug panel (Autos, Locals, or Watch windows).


## Debugging Features Reference

| Feature | Shortcut | Description |
|---------|----------|-------------|
| **Step Into** | `F11` | Step into a method call to debug inside the method |
| **Step Over** | `F10` | Execute the current line without stepping into method calls |
| **Step Out** | `Shift+F11` | Exit the current method and return to the caller |
| **Continue** | `F5` | Resume execution until the next breakpoint |
| **Restart** | `Ctrl+Shift+F5` | Restart the debugging session |
| **Stop** | `Shift+F5` | Stop the debugging session |

### Platform Consistency

**Important:** These debugging features, keyboard shortcuts, and debugging interface work identically across:

- WinForms applications
- WPF applications
- WinUI applications

The underlying .NET debugging experience in Syncfusion Code Studio remains consistent regardless of the desktop UI framework you're using.