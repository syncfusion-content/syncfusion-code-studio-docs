---
title: "Syncfusion Code Studio Languages"
description: "Professional guide for Swift development and debugging setup in Code Studio"
classification: "User Guide - Troubleshoot"
platform: syncfusion-code-studio
keywords: Swift, debugging, development, troubleshoot, code-studio, syncfusion
---

# Swift Development and Debugging Setup Guide for Code Studio (macOS)

This comprehensive guide will help you set up Swift development and debugging in Code Studio on macOS.

## Prerequisites

Before setting up Swift development in Code Studio, ensure you have the following prerequisites:

### 1. Install Xcode Command Line Tools
Open Terminal and run the following command:
```bash
xcode-select --install
```

If Xcode Command Line Tools are already installed, you'll see a message indicating they're already installed.

### 2. Install Xcode (Recommended)
1. Download Xcode from the [Mac App Store](https://apps.apple.com/us/app/xcode/id497799835)
2. Launch Xcode and accept the license agreement
3. Let Xcode install any additional components it requires

### 3. Verify Swift Installation
Open Terminal and run the following commands:
```bash
swift --version
```

If the command fails, ensure Xcode Command Line Tools are properly installed.

### 4. Install Swift Package Manager (Built-in)
Swift Package Manager comes bundled with Swift. Verify it's working:
```bash
swift package --version
```

## Code Studio Extensions Setup

### Required Extensions

To enable Swift development and debugging in Code Studio, you need to install the following extensions:

#### 1. Swift Extension
- **Purpose**: Provides language server protocol support for Swift, including syntax highlighting, code completion, and IntelliSense
- **Installation**: Search for "[Swift Extension Documentation](https://marketplace.visualstudio.com/items?itemName=sswg.swift-lang)" in the Extensions view (Cmd+Shift+X)

#### 2. CodeLLDB Debugger
- **Purpose**: Enables debugging capabilities for Swift applications with breakpoints, variable inspection, and step-through debugging
- **Installation**: Search for "[CodeLLDB Documentation](https://marketplace.visualstudio.com/items?itemName=vadimcn.vscode-lldb)" in the Extensions view (Cmd+Shift+X)

### Installation Steps

1. Open Code Studio
2. Navigate to Extensions view (Cmd+Shift+X)
3. Search for and install both "Swift" and "CodeLLDB" extensions
4. Restart Code Studio to activate the extensions

## Working with Swift Projects

### Opening Swift Development Projects

Once you have completed the setup, you can start working with Swift projects in Code Studio:

#### 1. Open a Swift Project
Use one of the following methods to open your Swift project:
- **File Menu**: Go to `File > Open Folder` and select your Swift project directory
- **Command Palette**: Press `Cmd+Shift+P`, type "Open Folder", and select your project directory

### Running Swift Projects

#### Using Terminal Execution
1. **Open Integrated Terminal**:
   - Press `Ctrl+`` (backtick) to open the terminal
   - Navigate to your file directory if needed
   
2. **Run Swift Code**:
   ```bash
   # Build and run a Swift package
   swift run
   
   # Build a Swift package
   swift build
   ```

#### Using Code Studio Run Features
1. **Run Swift File Directly**:
   - Open your Swift file (`.swift`)
   - Press `Cmd+F5` to run without debugging
   - Or use the Run button in the top-right corner

### Debugging Swift Projects

#### Setting Up Debug Configuration

1. **Create Launch Configuration**:
   - Open Run and Debug view (`Cmd+Shift+D`)
   - Click the "create a launch.json file" link
   - Select "LLDB" from the dropdown menu
   - Click the "Run and Debug" button

#### Quick Debug
1. **Debug Swift File**:
   - Open your Swift file (`.swift`)
   - Press `F5` to run with debugging
   - For single files, you might need to compile first:
     ```bash
     swiftc -g filename.swift -o main
     ```

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
- **Debug Console**: Evaluate Swift expressions during debugging using LLDB commands

## Troubleshooting

### Common Issues and Solutions

#### 1. Swift Not Recognized in Terminal
**Problem**: When running `swift --version`, you get "command not found: swift"

**Solutions**:
- Install Xcode Command Line Tools: `xcode-select --install`
- Verify Xcode Command Line Tools path:
  ```bash
  xcode-select -p
  ```
- Reset Xcode Command Line Tools path if needed:
  ```bash
  sudo xcode-select --reset
  ```
- Add Swift to PATH manually (if needed):
  ```bash
  echo 'export PATH="/usr/bin:$PATH"' >> ~/.zshrc
  source ~/.zshrc
  ```

#### 2. Debug Session Won't Start
**Problem**: Clicking F5 or "Run and Debug" doesn't start debugging session

**Solutions**:
- Ensure CodeLLDB extension is installed and enabled
- Build your Swift project first: `swift build`
- Check if your program path in `launch.json` is correct
- For single Swift files, compile with debug symbols:
  ```bash
  swiftc -g filename.swift -o main
  ```
- Update the `program` path in `launch.json` to point to your compiled binary
- Restart Code Studio after installing extensions

#### 3. Breakpoints Not Working
**Problem**: Breakpoints are set but debugger doesn't stop at them

**Solutions**:
- Ensure you're compiling with debug symbols (`-g` flag)
- Make sure you're running with debugging (`F5`) not just running (`Cmd+F5`)
- Check that breakpoints are set on executable lines (not comments or empty lines)
- Verify your Swift file is saved before debugging
- For Swift packages, ensure debug build: `swift build -c debug`
- Reload the window: Press `Cmd+Shift+P` and type "Developer: Reload Window"

#### 4. Swift Package Build Errors
**Problem**: Swift package won't build or run

**Solutions**:
- Check `Package.swift` file syntax
- Ensure all dependencies are properly declared
- Clean and rebuild:
  ```bash
  swift package clean
  swift build
  ```
- Update Swift Package Manager:
  ```bash
  swift package update
  ```