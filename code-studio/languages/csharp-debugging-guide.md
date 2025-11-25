---
title: Setup and Debug C# Applications in Syncfusion Code Studio
description: Step-by-step guide to setup and debug C# applications using Syncfusion Code Studio's debugging features and tools.
platform: syncfusion-code-studio
control: IDE
documentation: Troubleshoot
keywords: csharp, dotnet, .net, aspnetcore, debug, debugging, breakpoints, dotrush
---

# This Guide provides Step-By-Step Instructions for Setting-Up and Debugging C# Applications using Code Studio

## Language Setup

### Prerequisites

- Install the **.NET SDK** 6.0 or later from [.NET Downloads](https://dotnet.microsoft.com/download)
- Install **Syncfusion Code Studio**
- Install the **.NET CLI** (comes with .NET SDK)

### Verify .NET Installation

Open a terminal and run:
```
dotnet --version
```

Verify that your .NET SDK is detected and properly configured

## Required Extensions

To enable comprehensive C# debugging support, install the following extension:

### Essential Extension

**Dotrush**
- **Publisher**: tintoy/Tintoy Enterprises
- **Description**: Enhanced C# debugging experience with additional visualization and debugging utilities for .NET applications

## Configuration Steps

### Step 1: Install Extension

Open **Syncfusion Code Studio IDE**

Navigate to the **Extensions** view (`Ctrl+Shift+X`)

Search for "Dotrush"

Click **Install** on the Dotrush extension

Restart the IDE when prompted

### Step 2: Configure .NET Environment

**Method 1: Create a New .NET Project**
- Open **Command Palette** (`Ctrl+Shift+P`)
- Type `.NET: New Project`
- Select project type (Console, Web, Class Library, etc.)
- Enter project name and location

**Method 2: Open Existing .NET Project**
- Open the folder containing your .csproj file
- The IDE will automatically load the project
- Dotrush will automatically detect and configure the project

### Step 3: Create Launch Configuration

Open your C# project in Syncfusion Code Studio IDE

Go to **Run and Debug** view (`Ctrl+Shift+D`)

Click **create a launch.json file**

Select **.NET 5+ and .NET Core** environment

The IDE will create launch.json with basic configuration for debugging

## How to Run and Debug

Refer to [Common Debugging Steps](common-debugging-steps.md) for fundamental debugging procedures applicable to all languages.

### Language-Specific Debug Commands and Features

**C# and .NET-Specific Breakpoint Methods**
- **Exception Breakpoints**: Open **Run and Debug** view and expand **Breakpoints** section to configure exception types
- **DataTips**: Hover over variables in the code editor, pin DataTips to keep them visible

**C# and .NET-Specific Debug Methods**

**Method 1: Using Run and Debug View**
- Open **Run and Debug** view (`Ctrl+Shift+D`)
- Select your configuration from dropdown
- Click **Start Debugging** (`F5`)

**Method 2: Using Command Palette**
- Open **Command Palette** (`Ctrl+Shift+P`)
- Type `.NET: Debug`
- Select appropriate option

**Method 3: Quick Debug**
- Open C# file with Main method
- Press `F5` to debug current file
- IDE will build and start debugging automatically

**DataTips Enhancement**
- Hover over variables in the code editor
- Pin DataTips to keep them visible
- Click pin icon to lock DataTip position

## Debugging Different Project Types

### Console Applications

Use standard launch configuration

No special setup required beyond creating launch.json

### ASP.NET Core Applications

Add web browser debugging support

Set breakpoints in controller actions and middleware

Use web-specific configurations for launch.json

### Class Libraries

Debug using Unit Tests

Or create a console application that references the library

### Unit Tests

Install appropriate testing framework (xUnit, NUnit, MSTest)

Use the Testing view to run and debug tests

Click **Debug** above test method

Or use command palette: `.NET: Debug Test`

## Advanced Debugging Features

### Hot Reload

Enable automatic code reloading during debugging

Make code changes and see them apply without restarting

Supported in .NET 6+ with compatible project types

### Remote Debugging

Configure remote debugging for applications running on different machines

Use network-based debugging protocols

Set up secure connections for production debugging

### Just My Code

By default, the debugger steps through your code

Enable "Just My Code" to skip framework and library code

Disable to debug .NET framework and external libraries

## Troubleshooting Common Issues

### Issue 1: Debugger Not Starting

**Solutions:**
- Verify .NET SDK installation using `dotnet --version`
- Check omnisharp.dotnetPath setting in IDE preferences
- Restart IDE and clean workspace
- Delete bin and obj folders and rebuild project
- Ensure launch.json has correct configuration

### Issue 2: Breakpoints Not Hit

**Solutions:**
- Ensure code is compiled with debug information
- Verify breakpoint is in executable code path
- Check if code path actually reaches the breakpoint
- Clear workspace cache and rebuild solution
- Verify correct startup project is selected

### Issue 3: Source Not Found

**Solutions:**
- Verify source files are correctly located
- Check project paths in launch.json
- Ensure PDB debug files are generated
- Rebuild project with Debug configuration (not Release)

### Issue 4: Dotrush Not Detecting Project

**Solutions:**
- Ensure .csproj file is in the workspace root
- Restart the IDE
- Reload the current folder
- Check Dotrush output panel for specific errors

### Issue 5: Performance Issues

**Solutions:**
- Enable "Just My Code" to reduce debugging overhead
- Disable unnecessary breakpoints
- Increase IDE memory allocation
- Close unused debug sessions
- Avoid evaluating large objects in watch expressions

### Issue 6: Solution/Project Not Loading

**Solutions:**
- Ensure .sln or .csproj file exists in workspace root
- Check that all project references are valid
- Verify NuGet packages are restored (`dotnet restore`)
- Run `dotnet build` to check for compilation errors
- Verify Dotrush extension is properly installed and enabled
