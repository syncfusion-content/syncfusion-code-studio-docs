---
title: "Syncfusion Code Studio Languages"
description: "Professional guide for JavaScript development and debugging setup in Code Studio"
classification: "User Guide - Troubleshoot"
platform: syncfusion-code-studio
keywords: JavaScript, debugging, development, troubleshoot, code-studio, syncfusion
---

# JavaScript Development and Debugging Setup Guide for Code Studio

This comprehensive guide will help you set up JavaScript development and debugging in Code Studio.

## Code Studio Extensions Setup

### Required Extensions

To enable JavaScript development and debugging in Code Studio, you need to install the following extensions:

#### 1. Live Server Extension
- **Purpose**: Launches a local development server with live reload feature for static and dynamic pages
- **Installation**: Search for "[Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)" in the Extensions view (Ctrl+Shift+X)

### Installation Steps

1. Open Code Studio
2. Navigate to Extensions view (Ctrl+Shift+X)
3. Search for and install the 'Live Server' extension
4. Restart Code Studio to activate the extension

## Working with JavaScript Projects

### Opening JavaScript Projects

#### 1. Open a JavaScript Project
Use one of the following methods to open your JavaScript project:
- **File Menu**: Go to `File > Open Folder` and select your project directory
- **Command Palette**: Press `Ctrl+Shift+P`, type "Open Folder", and select your project directory

### Running JavaScript Projects

#### Using Live Server (for Browser-based JavaScript)
1. **Install Live Server Extension** (if not already installed)
2. **Right-click on your `index.html` file**
3. **Select "Open with Live Server"**
4. Your browser will open automatically with your application

#### Using Code Studio Run Features
1. **Run JavaScript File**:
   - Open your JavaScript file (`.js`)
   - Press `Ctrl+F5` to run without debugging
   - Or use the Run button in the top-right corner

### Debugging JavaScript Projects

#### Setting Up Debug Configuration

##### For Browser-based JavaScript Applications
1. **Create Launch Configuration**:
   - Open Run and Debug view (`Ctrl+Shift+D`)
   - Click the "create a launch.json file" link
   - Select "Web App (Chrome)" or "Web App (Edge)"
   - Automatically configure the current file path
   - Select the configuration and run

#### Quick Debug
1. **Debug JavaScript File**:
   - Open your JavaScript file (`.js`)
   - Press `F5` to run with debugging
   - For browser-based files, ensure your local server is running

#### Debugging Features

Once debugging is active, you can use the following features:
- **Set Breakpoints**: Click in the gutter next to line numbers or press `F9`
- **Step Through Code**: 
  - `F10` - Step Over
  - `F11` - Step Into 
  - `Shift+F11` - Step Out
  - `F5` - Continue
- **Inspect Variables**: Hover over variables or use the Variables panel
- **Watch Expressions**: Add expressions to the Watch panel
- **Debug Console**: Evaluate JavaScript expressions during debugging
- **Call Stack**: View the current execution stack

## Troubleshooting

### Common Issues and Solutions

#### 1. Debug Session Won't Start
**Problem**: Clicking F5 or "Run and Debug" doesn't start debugging session

**Solutions**:
- **For Browser-based Apps**:
  - Ensure your local server is running
  - Check if the URL in `launch.json` matches your server URL
  - Verify your HTML file path is correct
- **General**:
  - Restart Code Studio
  - Check the Debug Console for error messages

#### 2. Breakpoints Not Working
**Problem**: Breakpoints are set but debugger doesn't stop at them

**Solutions**:
- **Browser-based JavaScript**:
  - Enable source maps in browser developer tools
  - Ensure you're debugging (F5) not just running (Ctrl+F5)
  - Check that breakpoints are set on executable lines (not comments or empty lines)
  - Clear browser cache and restart debugging session
- **General**:
  - Reload the window: Press `Ctrl+Shift+P` and type "Developer: Reload Window"