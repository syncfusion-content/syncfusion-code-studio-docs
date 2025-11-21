---
title: "Syncfusion Code Studio Languages"
description: "Professional guide for Ruby development and debugging setup in Code Studio"
classification: "User Guide - Troubleshoot"
platform: syncfusion-code-studio
keywords: Ruby, debugging, development, troubleshoot, code-studio, syncfusion
---

# Ruby Development and Debugging Setup Guide for Code Studio

This comprehensive guide will help you set up Ruby development and debugging in Code Studio.

## Prerequisites

Before setting up Ruby development in Code Studio, ensure you have the following prerequisites:

### 1. Install Ruby
1. Download Ruby from [rubyinstaller.org](https://rubyinstaller.org/downloads/)
2. Choose **Ruby+Devkit version** (recommended: Ruby 3.1 or higher)
3. During installation:
   - Check "Add Ruby executables to your PATH"
   - Accept the default installation directory

### 2. Verify Ruby Installation
Open PowerShell as Administrator and run the following commands:
```powershell
ruby --version
gem --version
```

If any command fails or shows an error, restart your terminal or computer and try again.

### 3. Update RubyGems (Optional but Recommended)
Open PowerShell as Administrator and execute the following commands:
```powershell
# Update RubyGems system
gem update --system

# Install Rails framework (optional, if needed for your projects)
gem install rails
```

## Code Studio Extensions Setup

### Required Extensions

To enable Ruby development and debugging in Code Studio, you need to install the following extensions:

#### 1. Ruby LSP
- **Purpose**: Provides language server protocol support for Ruby, including syntax highlighting, code completion, and IntelliSense
- **Installation**: Search for "[Ruby LSP Extension Documentation](https://marketplace.visualstudio.com/items?itemName=Shopify.ruby-lsp)" in the Extensions view (Ctrl+Shift+X)

#### 2. VSCode rdbg Ruby Debugger
- **Purpose**: Enables debugging capabilities for Ruby applications with breakpoints, variable inspection, and step-through debugging
- **Installation**: Search for "[VSCode rdbg Ruby Debugger Documentation](https://marketplace.visualstudio.com/items?itemName=KoichiSasada.vscode-rdbg)" in the Extensions view (Ctrl+Shift+X)

### Installation Steps

1. Open Code Studio
2. Navigate to Extensions view (Ctrl+Shift+X)
3. Search for and install both "Ruby LSP" and "VSCode rdbg Ruby Debugger" extensions
4. Restart Code Studio to activate the extensions

## Required Ruby Gems

Install the necessary debugging gem:

```powershell
# For Ruby debugging support
gem install debug
```

## Working with Ruby Projects

### Opening Ruby Development Projects

Once you have completed the setup, you can start working with Ruby projects in Code Studio:

#### 1. Open a Ruby Project
Use one of the following methods to open your Ruby project:
- **File Menu**: Go to `File > Open Folder` and select your Ruby project directory
- **Command Palette**: Press `Ctrl+Shift+P`, type "Open Folder", and select your project directory
- **Drag and Drop**: Drag your project folder directly into Code Studio

### Running Ruby Projects

#### Using Code Studio Run Features
1. **Run Ruby File Directly**:
   - Open your Ruby file (`.rb`)
   - Press `Ctrl+F5` to run without debugging
   - Or right-click in the editor and select "Run Ruby"

#### Using Terminal Execution
1. **Open Integrated Terminal**:
   - Press `Ctrl+`` (backtick) to open the terminal
   - Navigate to your file directory if needed
   
2. **Run the Ruby File**:
   ```powershell
   # Run a single Ruby file
   ruby filename.rb
   ```

### Debugging Ruby Projects

#### Quick Debug
1. **Debug Ruby File Directly**:
   - Open your Ruby file (`.rb`)
   - Press `F5` to run with debugging
   - Or right-click in the editor and select "Debug Ruby"

#### Using Debug Panel
1. **Set Up Debug Configuration**:
   - Open Run and Debug view (`Ctrl+Shift+D`)
   - Click "Run and Debug" button
   - Click the "create a launch.json file" link
   - Select "Ruby rdbg" from the dropdown menu
   - Choose "Debug current file with rdbg" option
   
2. **Launch Debug Session**:
   - Code Studio will execute your Ruby file with debugging capabilities
   - The debug toolbar will appear at the top of the editor

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
- **Debug Console**: Evaluate Ruby expressions during debugging

## Troubleshooting

### Common Issues and Solutions

#### 1. Ruby Not Recognized in Terminal
**Problem**: When running `ruby --version`, you get "'ruby' is not recognized as an internal or external command"

**Solutions**:
- Restart Code Studio and your computer after Ruby installation
- Verify Ruby is installed and added to PATH:
  ```powershell
  # Check if Ruby is in PATH
  echo $env:PATH
  
  # Manually add Ruby to PATH if needed (adjust path as needed)
  $env:PATH += ";C:\Ruby32-x64\bin"
  ```
- Reinstall Ruby with "Add Ruby executables to your PATH" option checked

#### 2. Debug Session Won't Start
**Problem**: Clicking F5 or "Run and Debug" doesn't start debugging session

**Solutions**:
- Install the `debug` gem: `gem install debug`
- Verify Code Studio rdbg Ruby Debugger extension is installed and enabled
- Check if `launch.json` configuration is correct
- Try creating a new `launch.json` file:
  - Open Run and Debug view (`Ctrl+Shift+D`)
  - Click "create a launch.json file"
  - Select "Ruby rdbg"
- Restart Code Studio after installing extensions

#### 3. Breakpoints Not Working
**Problem**: Breakpoints are set but debugger doesn't stop at them

**Solutions**:
- Ensure you're running with debugging (`F5`) not just running (`Ctrl+F5`)
- Verify the `debug` gem is installed: `gem list debug`
- Check that breakpoints are set on executable lines (not comments or empty lines)
- Make sure your Ruby file is saved before debugging
- Reload the window: Press `Ctrl+Shift+P` and type "Developer: Reload Window"
- For advanced debugging techniques, refer to this [Ruby trace inspector guide](https://dev.to/ono-max/intro-to-trace-inspector-that-displays-ruby-trace-logs-with-pretty-ui-3pi7)