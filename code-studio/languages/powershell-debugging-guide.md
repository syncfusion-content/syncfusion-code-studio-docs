---
title: Setup and Debug PowerShell Applications in Syncfusion Code Studio
description: Step-by-step guide to setup and debug PowerShell applications using Syncfusion Code Studio's debugging features and tools.
platform: syncfusion-code-studio
control: IDE
documentation: Troubleshoot
keywords: powershell, script analyzer, debugger, breakpoints, debug
---

# This Guide provides Step-By-Step Instructions for Setting-Up and Debugging PowerShell Applications using Code Studio

## Language Setup

### Prerequisites

- Install **PowerShell 7.2** or later from [PowerShell GitHub](https://github.com/PowerShell/PowerShell/releases)
- Or use **Windows PowerShell 5.1** (Windows-only) with .NET Framework 4.8

### Verify PowerShell Installation

Open the **Command Palette** (`Ctrl+Shift+P`)

Type `PowerShell: Show Session Menu` and select it

Verify that your PowerShell version is displayed and properly configured

## Required Extensions

To enable comprehensive PowerShell debugging support, install the following extensions:

### Essential Extensions

**PowerShell**
- **Publisher**: Microsoft
- **Description**: Language support for PowerShell, debugging capabilities, script analysis, IntelliSense, and code snippets

The PowerShell extension includes:

**PowerShell Debugger**
- Built-in support for local and remote debugging
- Breakpoints, step through code, variable inspection

**PSScriptAnalyzer**
- Static code analysis for PowerShell scripts
- Best practices recommendations and code quality checks

## Configuration Steps

### Step 1: Install Extensions

Open **Syncfusion Code Studio IDE**

Navigate to the **Extensions** view (`Ctrl+Shift+X`)

Search for "PowerShell"

Click **Install** on the PowerShell extension by Microsoft

Restart the IDE when prompted

### Step 2: Choose PowerShell Version

Open **Command Palette** (`Ctrl+Shift+P`)

Type `PowerShell: Show Session Menu` and select it

Choose your preferred PowerShell version from the list

The selected version appears in the Status Bar at the bottom right

### Step 3: Create Launch Configuration

**For No-Workspace Debugging:**
- Open a PowerShell script file using File > Open File
- Set a breakpoint and press F5 to start debugging immediately

**For Workspace Debugging:**
- Open a folder containing your PowerShell project
- Go to **Run and Debug** view (`Ctrl+Shift+D`)
- Click **create a launch.json file**
- Select **PowerShell** environment
- The IDE will create launch.json with debug configurations

## How to Run and Debug

Refer to [Common Debugging Steps](common-debugging-steps.md) for fundamental debugging procedures applicable to all languages.

### Language-Specific Debug Commands and Features

**PowerShell-Specific Breakpoint Methods**
- **Programmatic Breakpoints**: Use `Set-PSBreakpoint` cmdlet in PowerShell code to set breakpoints on lines, functions, or variables
- **Breakpoint Persistence**: Breakpoints persist in the Extension Terminal

**PowerShell-Specific Debug Methods**

**Method 1: Using Run and Debug View**
- Open **Run and Debug** view (`Ctrl+Shift+D`)
- Select your configuration from dropdown
- Click **Start Debugging** (`F5`)

**Method 2: Quick Debug (No-Workspace)**
- Open PowerShell script file
- Press `F5` to start debugging
- Debugger stops at first breakpoint or runs to completion

**Method 3: Using Command Palette**
- Open **Command Palette** (`Ctrl+Shift+P`)
- Type `Debug PowerShell Script`
- Select appropriate option

**Method 4: Run in Extension Terminal**
- Use Extension Terminal to run commands interactively
- Debugger attaches automatically to commands in terminal

**PowerShell-Specific Debug Console**
- Evaluate PowerShell expressions during debugging
- Type PowerShell cmdlets and press Enter to execute
- Useful for inspecting objects and testing code

## Debugging Different Project Types

### Standard PowerShell Scripts

Use the default launch configuration to debug .ps1 script files

### PowerShell Modules

Debug module files and manifest files

## Advanced Debugging Features

### Interactive Session Debugging

Debug commands executed from the Extension Terminal

Terminal integrates with debugger automatically

### Multi-version Support

Switch between PowerShell versions without restarting

Use PowerShell: Show Session Menu to change versions

Each version has separate debugging session

## Unit Test Debugging

### Debug Single Test

Open test file

Click **Debug** above test function

Test executes in debug mode with breakpoints active

### Debug All Tests

Right-click test file

Select **Run Tests** or **Debug Tests**

All tests in the file run in debug mode

## Troubleshooting Common Issues

### Issue 1: Debugger Not Starting

**Solutions:**
- Verify PowerShell installation and version
- Check selected PowerShell version in Status Bar
- Use `PowerShell: Show Session Menu` to select correct version
- Restart IDE and check extension status
- Verify launch.json has correct PowerShell configuration

### Issue 2: Breakpoints Not Hit

**Solutions:**
- Ensure script file is saved before debugging
- Verify breakpoint is on executable code
- Check if code path actually reaches the breakpoint
- Clear all breakpoints and set them again
- Verify PowerShell version supports the breakpoint

### Issue 3: Extension Terminal Not Available

**Solutions:**
- Ensure PowerShell extension is properly installed
- Check extension status in Extensions view
- Verify PowerShell version is compatible
- Reinstall extension if terminal doesn't appear

### Issue 4: Variables Not Visible During Debug

**Solutions:**
- Ensure variables are in scope during debugging
- Check if variables are declared before breakpoint
- Expand object properties in Variables panel
- Use Watch panel to monitor specific expressions

### Issue 5: Script Execution Issues

**Solutions:**
- Verify script syntax is correct
- Check execution policy settings
- Ensure script has proper permissions
- Review error messages in Debug Console
