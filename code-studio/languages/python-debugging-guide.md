---
title: Setup and Debug Python Applications in Syncfusion Code Studio
description: Step-by-step guide to setup and debug Python applications using Syncfusion Code Studio's debugging features and tools.
platform: syncfusion-code-studio
control: IDE
documentation: Troubleshoot
keywords: python, debugpy, debug, debugging, breakpoints
---

# This Guide provides Step-By-Step Instructions for Setting-Up and Debugging Python Applications using Code Studio

## Language Setup

### Prerequisites

- Install **Python** 3.7 or later from [Python.org](https://www.python.org/downloads/)
- Install **pip** (Python package installer, usually comes with Python)

### Verify Python Installation

Open the **Command Palette** (`Ctrl+Shift+P`)

Type `Python: Select Interpreter` and select it

Verify that your Python interpreter is detected and properly configured

## Required Extensions

To enable comprehensive Python debugging support, install the following extensions:

### Essential Extensions

**Python**
- **Publisher**: Microsoft
- **Description**: IntelliSense, Linting, Debugging, code navigation, code formatting, refactoring, variable explorer, test explorer, and more

**Python Debugger**
- **Publisher**: Microsoft
- **Description**: A debugger for Python with support for local and remote debugging, including debugging in Docker containers and Virtual environments

## Configuration Steps

### Step 1: Install Extensions

Open **Syncfusion Code Studio IDE**

Navigate to the **Extensions** view (`Ctrl+Shift+X`)

Search for "Python"

Click **Install** on the Python extension by Microsoft

Install the **Python Debugger** extension as well

Restart the IDE when prompted

### Step 2: Configure Python Environment

**Method 1: Using Python: Select Interpreter**
- Open **Command Palette** (`Ctrl+Shift+P`)
- Type `Python: Select Interpreter` and select it
- Choose your preferred Python interpreter from the list
- The selected interpreter appears in the Status Bar at the bottom right

**Method 2: Using Environment Variable**
- Set `PYTHONPATH` environment variable to your Python installation path
- Add Python installation `\Scripts` directory to your system PATH

### Step 3: Create Launch Configuration

Open your Python project in Syncfusion Code Studio IDE

Go to **Run and Debug** view (`Ctrl+Shift+D`)

Click **create a launch.json file**

Select **Python Debugger** environment

The IDE will create launch.json with basic configuration for debugging

## How to Run and Debug

Refer to [Common Debugging Steps](common-debugging-steps.md) for fundamental debugging procedures applicable to all languages.

### Language-Specific Debug Commands and Features

**Python-Specific Breakpoint Methods**
- **Inline Breakpoints**: Use `debugpy.breakpoint()` in your Python code to programmatically set a breakpoint
- **Hit Count Operators**: Conditional breakpoints support hit count operators (>, >=, <, <=, ==, %)

**Python-Specific Debug Methods**

**Method 1: Using Run and Debug View**
- Open **Run and Debug** view (`Ctrl+Shift+D`)
- Select your configuration from dropdown
- Click **Start Debugging** (`F5`)

**Method 2: Using Command Palette**
- Open **Command Palette** (`Ctrl+Shift+P`)
- Type `Debug Python File` or `Python: Debug Current File`
- Select appropriate option

**Method 3: Quick Debug**
- Click the debug button (play icon with a bug) in the top-right corner of the editor
- Or use the down-arrow to select **Python Debugger: Debug Python File**

**Method 4: Debug from Command Line**
- Install debugpy using pip
- Run with debugger from terminal
- Then attach VS Code debugger using attach configuration

**Hover Inspection**
- Hover mouse over variables in the code
- View variable values in a tooltip
- Quick way to inspect values without using panels

## Debugging Different Project Types

### Standard Python Scripts

Use the default configuration to debug Python files

## Advanced Debugging Features

### Hot Code Reload

Enable automatic code reloading during debugging when changes are made to code after the debugger execution has hit a breakpoint

Code changes are automatically applied without restarting the session

### Multi-threaded Debugging

Enable subprocess debugging for multi-threaded applications

Allows the debugger to attach to subprocesses created by the main process

### Environment Variables

Set environment variables for debugging session using the env property

Specify environment variable definitions file using envFile property

Variables are passed to the Python process during debugging

### Just My Code

By default, the debugger only steps through user-written code

Set justMyCode: false to also debug standard library functions

## Unit Test Debugging

### Debug Single Test

Open test file (using pytest or unittest framework)

Click **Debug** above test method

Or use command palette: `Python: Debug Tests`

### Debug All Tests

Right-click test file

Select **Run Tests** or **Debug Tests**

All tests in the file run in debug mode with breakpoints active

## Troubleshooting Common Issues

### Issue 1: Debugger Not Starting

**Solutions:**
- Verify Python installation using standard terminal commands
- Check selected interpreter in Status Bar (bottom right)
- Use `Python: Select Interpreter` command to select correct Python
- Restart IDE and clean workspace cache
- Verify launch.json has correct `"type": "debugpy"` (not deprecated `"python"`)

### Issue 2: Breakpoints Not Hit

**Solutions:**
- Ensure file is saved before debugging
- Verify breakpoint is on executable code (not on blank lines or comments)
- Check if code path actually reaches the breakpoint
- Clear all breakpoints and set them again
- Verify the correct Python interpreter is selected

### Issue 3: "Source Not Found" Error

**Solutions:**
- Verify Python source files are in workspace
- Check pathMappings configuration for remote debugging
- Rebuild/reinstall packages if needed

### Issue 4: Module Import Errors

**Solutions:**
- Install required packages using pip
- Check PYTHONPATH is correctly configured
- Ensure current working directory (cwd) in launch.json is correct

### Issue 5: Performance Issues During Debugging

**Solutions:**
- Disable unnecessary breakpoints
- Use `justMyCode: true` to skip debugging standard library
- Increase IDE memory allocation
- Close unused debug sessions
- Avoid debugging very large data structures in watch expressions
