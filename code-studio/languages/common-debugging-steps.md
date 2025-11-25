---
title: Common Debugging Steps in Syncfusion Code Studio
description: Universal debugging steps applicable to all programming languages in Syncfusion Code Studio.
platform: syncfusion-code-studio
control: IDE
documentation: Troubleshoot
keywords: debug, debugging, breakpoints, common-steps, universal
---

# Common Debugging Steps in Syncfusion Code Studio

This guide covers the fundamental debugging steps that apply across all programming languages supported in Syncfusion Code Studio.

## Step 1: Set Breakpoints

**Line Breakpoints**
- Click in the gutter next to the line number
- Red dot appears indicating breakpoint is set
- Or press `F9` while cursor is on the line

**Conditional Breakpoints**
- Right-click on breakpoint
- Select **Edit Breakpoint**
- Enter condition for when breakpoint should trigger

**Logpoints**
- Right-click in gutter
- Select **Add Logpoint**
- Enter message to log without stopping execution
- Useful for tracing execution flow

**Exception Breakpoints**
- Open **Run and Debug** view (`Ctrl+Shift+D`)
- Expand **Breakpoints** section
- Check boxes for exception types to pause on

## Step 2: Start Debugging

**Method 1: Using Run and Debug View**
- Open **Run and Debug** view (`Ctrl+Shift+D`)
- Select your configuration from dropdown
- Click **Start Debugging** (`F5`)

**Method 2: Using Command Palette**
- Open **Command Palette** (`Ctrl+Shift+P`)
- Type appropriate debug command for your language
- Select from available options

**Method 3: Quick Debug**
- Press `F5` to debug current file
- IDE will automatically build and start debugging

## Step 3: Debug Navigation Controls

Once debugging starts, use these keyboard shortcuts:

- **Continue** (`F5`): Resume execution
- **Step Over** (`F10`): Execute next line, skip function calls
- **Step Into** (`F11`): Enter function calls
- **Step Out** (`Shift+F11`): Exit current function
- **Restart** (`Ctrl+Shift+F5`): Restart debugging session
- **Stop** (`Shift+F5`): Stop debugging

## Step 4: Inspect Variables and Data

**Variables Panel**
- View local variables, parameters, and properties
- Expand objects to see properties and nested values
- Modify variable values during debugging to test scenarios

**Watch Expressions**
- Add expressions to monitor their values
- Right-click variable → **Add to Watch**
- Or manually add in Watch panel

**Debug Console**
- Evaluate expressions during debugging
- Access via **Debug Console** tab at the bottom
- Type expressions and press Enter to evaluate

**Hover Inspection**
- Hover mouse over variables in the code
- View variable values in a tooltip
- Quick way to inspect values without using panels

## Step 5: Navigate Call Stack

- **Call Stack Panel** shows the execution path
- Click on stack frames to navigate between function calls
- See function/method names and line numbers
- Understand program flow and call hierarchy
