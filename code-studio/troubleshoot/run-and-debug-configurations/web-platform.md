---
title: Debug Web Platform Applications in Syncfusion Code Studio
description: Comprehensive guide to debug ASP.NET Core Web and Blazor WebAssembly applications using Syncfusion Code Studio's debugging features and tools.
platform: syncfusion-code-studio
control: IDE
documentation: Troubleshoot
keywords: web platform, asp.net core, blazor webassembly, debug, debugging, breakpoints, browser tools, server-side, client-side, troubleshoot, code-studio, dotrush
---

# Debugging Web Platform Applications in Syncfusion Code Studio

## Overview

**Syncfusion Code Studio** provides comprehensive debugging capabilities for modern web platform applications, including both server-side ASP.NET Core applications and client-side Blazor WebAssembly applications. This guide covers debugging techniques, configuration setup, and best practices for web platform development using the **DotRush** debugger and integrated browser tools.

## Prerequisites

- **Syncfusion Code Studio** installed on your system
- **.NET SDK 9.0** installed based on your platform (Windows, macOS, or Linux). Download from the [.NET Website](https://dotnet.microsoft.com/)
- **Verify .NET SDK installation** by running the following commands in the terminal:
  - Check version: `dotnet --version`
  - Get detailed information: `dotnet --info`
- **Modern web browser** (Chrome, Edge, Firefox) with WebAssembly debugging support (for Blazor WASM)
- **Required workloads** installed:

  **For ASP.NET Core:**
  ```bash
  dotnet --list-sdks
  ```

  **For Blazor WebAssembly:**
  ```bash
  dotnet workload install wasm-tools
  ```

  **Verify installations:**
  ```bash
  dotnet new list
  dotnet workload list
  ```

## Built-in Extensions of Code Studio

Syncfusion Code Studio comes with pre-installed extensions that enhance web platform development and debugging capabilities for both server-side and client-side applications.

**For detailed information about Code Studio's built-in extensions, see:** [Built-in Extensions of Syncfusion Code Studio](../../built-in-extensions.md)

This guide covers debugging for Below web platform:

1. **[ASP.NET Core Web Applications](#aspnet-core-web-applications)** - Server-side web applications
2. **[Blazor WebAssembly Applications](#blazor-webassembly-applications)** - Client-side web applications

---

# ASP.NET Core Web Applications

ASP.NET Core is a server-side web application framework that runs on the server and generates HTML, CSS, and JavaScript that is sent to the client's web browser.

## Overview

Debugging is an essential part of the ASP.NET Core web development process that helps identify and fix issues in your server-side applications. This section provides step-by-step instructions for effectively debugging your ASP.NET Core web applications using the **DotRush** debugger.

## Create an ASP.NET Core Web Project

Before you can debug an ASP.NET Core application, you need to set up a project. Follow these steps to create a new ASP.NET Core web project in Syncfusion Code Studio:

### Step 1: Create a Solution
1. Open Syncfusion Code Studio.
2. Navigate to **Solution** > **Create New Solution**.
3. Create a new solution by specifying the **solution name**.

### Step 2: Add an ASP.NET Core Project to the Solution
1. Right-click on the solution in the **Solution Explorer** panel.
2. Select **Add New Project** from the context menu.
3. In the project template selection:
   - Choose the **ASP.NET Core Web App** template
   - Specify your **application name**
   - Set the **project location**

## Steps to Run and Debug an ASP.NET Core Application

Once you have created your ASP.NET Core project, follow these comprehensive steps to configure, build, and debug your application effectively.

### Configure Code Studio for Building the Project

#### Step 1: Set Up Debug Configuration Files

1. Navigate to the **Run and Debug** section and create the `launch.json` file using the **.NET Core Debugger**.

2. Create a `tasks.json` file within the `.vscode` folder.

#### Step 2: Configure tasks.json for ASP.NET Core

Create the following `tasks.json` file in your `.vscode` folder:

```json
{
    "version": "2.0.0",
    "tasks": [
        {
            "label": "build",
            "command": "dotnet",
            "type": "process",
            "args": [
                "build",
                "${workspaceFolder}/YourWebApp/YourWebApp.csproj",
                "/property:GenerateFullPaths=true",
                "/consoleloggerparameters:NoSummary"
            ],
            "problemMatcher": "$msCompile",
            "group": {
                "kind": "build",
                "isDefault": true
            }
        },
        {
            "label": "publish",
            "command": "dotnet",
            "type": "process",
            "args": [
                "publish",
                "${workspaceFolder}/YourWebApp/YourWebApp.csproj",
                "/property:GenerateFullPaths=true",
                "/consoleloggerparameters:NoSummary"
            ],
            "problemMatcher": "$msCompile"
        },
        {
            "label": "watch",
            "command": "dotnet",
            "type": "process",
            "args": [
                "watch",
                "run",
                "--project",
                "${workspaceFolder}/YourWebApp/YourWebApp.csproj"
            ],
            "problemMatcher": "$msCompile"
        },
        {
            "label": "clean",
            "command": "dotnet",
            "type": "process",
            "args": [
                "clean",
                "${workspaceFolder}/YourWebApp/YourWebApp.csproj"
            ],
            "problemMatcher": "$msCompile"
        }
    ]
}
```

#### Step 3: Configure launch.json for ASP.NET Core

Create the following `launch.json` file in your `.vscode` folder:

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Launch ASP.NET Core Web App",
            "type": "coreclr",
            "request": "launch",
            "preLaunchTask": "build",
            "program": "${workspaceFolder}/Your-Asp-core/bin/Debug/net9.0/Your-Asp-core.dll",
            "args": [],
            "cwd": "${workspaceFolder}/Your-Asp-core",
            "serverReadyAction": {
                "action": "openExternally",
                "pattern": "\\bNow listening on:\\s+(https?://\\S+)"
            },
            "env": {
                "ASPNETCORE_ENVIRONMENT": "Development"
            },
            "sourceFileMap": {
                "/Views": "${workspaceFolder}/Your-Asp-core/Views",
                "/Pages": "${workspaceFolder}/Your-Asp-core/Pages"
            },
            "console": "integratedTerminal",
            "internalConsoleOptions": "openOnSessionStart"
        }
    ]
}
```

## ASP.NET Core Project Structure

### Verify File Structure

Your ASP.NET Core project structure should look like this:

```
YourSolution/
├── .vscode/
│   ├── tasks.json
│   └── launch.json
└── YourWebApp/
    ├── Pages/
    ├── Models/
    ├── wwwroot/
    ├── Program.cs
    ├── appsettings.json
    └── YourWebApp.csproj
```

## Running the ASP.NET Core Application

### Build the Project

Before running the application, build your project to ensure all dependencies are properly configured:

```bash
# Navigate to project directory
cd YourWebApp

# Build the project
dotnet build
```

### Running via Code Studio Debug

1. Go to **Run and Debug** in the Activity Bar
2. Select **Launch ASP.NET Core Web App** from the dropdown
3. Click the **Start Debugging** button or press `F5`

### Running via Terminal

For quick building and running without debugging, use these terminal commands:

```bash
# Navigate to project directory
cd YourWebApp

# Run the application
dotnet run

# Run with hot reload (recommended for development)
dotnet watch run
```

# Blazor WebAssembly Applications

Blazor WebAssembly is a client-side web application framework that runs C# code directly in the web browser using WebAssembly, providing a rich interactive user experience without requiring server round-trips.

## Overview

Debugging Blazor WebAssembly applications requires specialized tools and techniques due to their client-side execution model. This section demonstrates how to configure, debug, and troubleshoot Blazor WASM applications using the **DotRush** debugger and browser development tools.

## Create a Blazor WebAssembly Project

### Step 1: Initialize Solution
- Open Syncfusion Code Studio
- Navigate to **Solution** > **Create New Solution**
- Specify solution name and location

### Step 2: Add Blazor WASM Project
- Right-click the solution in **Solution Explorer**
- Select **Add New Project**
- Choose the **Blazor WebAssembly App** template
- Configure the project name and location

## Blazor WebAssembly Debug Configuration

### Configure Debug Environment

#### Step 1: Create Configuration Files

Create the necessary debugging configuration files in your project's `.vscode` directory:

1. Navigate to the **Run and Debug** panel
2. Generate `launch.json` for Blazor WebAssembly debugging
3. Create `tasks.json` for build automation

#### Step 2: Tasks Configuration for Blazor WASM

Create the following `tasks.json` file in your `.vscode` folder:

```json
{
    "version": "2.0.0",
    "tasks": [
        {
            "label": "build",
            "command": "dotnet",
            "type": "process",
            "args": [
                "build",
                "${workspaceFolder}/YourBlazorApp/YourBlazorApp.csproj",
                "/property:GenerateFullPaths=true",
                "/consoleloggerparameters:NoSummary"
            ],
            "problemMatcher": "$msCompile",
            "group": {
                "kind": "build",
                "isDefault": true
            }
        },
        {
            "label": "publish",
            "command": "dotnet",
            "type": "process",
            "args": [
                "publish",
                "${workspaceFolder}/YourBlazorApp/YourBlazorApp.csproj",
                "/property:GenerateFullPaths=true",
                "/consoleloggerparameters:NoSummary"
            ],
            "problemMatcher": "$msCompile"
        },
        {
            "label": "watch",
            "command": "dotnet",
            "type": "process",
            "args": [
                "watch",
                "run",
                "--project",
                "${workspaceFolder}/YourBlazorApp/YourBlazorApp.csproj"
            ],
            "problemMatcher": "$msCompile"
        },
        {
            "label": "clean",
            "command": "dotnet",
            "type": "process",
            "args": [
                "clean",
                "${workspaceFolder}/YourBlazorApp/YourBlazorApp.csproj"
            ],
            "problemMatcher": "$msCompile"
        }
    ]
}
```

#### Step 3: Launch Configuration for Blazor WASM

Create the following `launch.json` file in your `.vscode` folder:

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Launch Blazor WebAssembly in Chrome",
            "type": "blazorwasm",
            "request": "launch",
            "cwd": "${workspaceFolder}/YourBlazorApp",
            "browser": "chrome"
        },
        {
            "name": "Launch Blazor WebAssembly in Edge",
            "type": "blazorwasm",
            "request": "launch",
            "cwd": "${workspaceFolder}/YourBlazorApp",
            "browser": "edge"
        }
    ]
}
```

## Blazor WebAssembly Project Structure

### Verify File Structure

Your Blazor WebAssembly project structure should look like this:

```
YourSolution/
├── .vscode/
│   ├── tasks.json
│   └── launch.json
└── YourBlazorApp/
    ├── Components/
    ├── Pages/
    ├── wwwroot/
    ├── Program.cs
    ├── App.razor
    └── YourBlazorApp.csproj
```

## Running the Blazor WebAssembly Application

### Build the Project

Before running the application, build your project to ensure all dependencies are properly configured:

```bash
# Navigate to project directory
cd YourBlazorApp

# Build the project
dotnet build
```

### Running via Code Studio Debug

1. **Build Project:** Ensure all dependencies are properly configured before debugging
2. **Select Debug Target:** Choose a browser-specific debugging configuration
3. **Start Debugging:** Use the **Run and Debug** panel or press `F5`

### Browser-Specific Debugging

| Browser | Configuration | Features |
|---------|---------------|----------|
| **Chrome** | `Launch Blazor WebAssembly in Chrome` | Advanced WebAssembly debugging tools |
| **Edge** | `Launch Blazor WebAssembly in Edge` | Enhanced Microsoft debugging integration |

### Running via Terminal

**Terminal Commands:**
```bash
# Navigate to project directory
cd YourBlazorApp

# Run the application
dotnet run

# Development with hot reload
dotnet watch run
```

---

# Important Notes

Before proceeding with debugging your web platform applications in Code Studio, please consider these critical points:

- **File Structure:** The `.vscode` folder should be at the same level as your solution folder to ensure proper configuration loading.

- **Relative Paths:** All file paths in the configuration files are relative to the workspace root. Ensure your workspace is properly set up.

- **Project Name Matching:** The project name in configuration files must exactly match your `.csproj` file name. Any mismatch will cause build failures.

- **Port Configuration:** Ensure the ports specified in `launchSettings.json` and environment variables don't conflict with other running applications.

- **HTTPS Development Certificate:** For HTTPS debugging, ensure you have a valid development certificate installed by running `dotnet dev-certs https --trust`.

- **Hot Reload Support:** Use `dotnet watch run` for automatic rebuilding and reloading during development.

- **Breakpoint Functionality:** Server-side breakpoints in controllers, services, and middleware work reliably with the DotRush debugger.

- **WebAssembly Requirements:** Chrome/Edge are recommended for optimal WebAssembly debugging. Ensure your browser supports WebAssembly debugging features.

## Video Tutorial

For a comprehensive visual guide on web platform development and debugging, refer to Microsoft's official documentation and video tutorials.

**ASP.NET Core Resources:**
- [ASP.NET Core Debugging Documentation](https://docs.microsoft.com/aspnet/core/test/debugging)
- [Entity Framework Core Logging](https://docs.microsoft.com/ef/core/logging-events-diagnostics/)
- [ASP.NET Core Performance Best Practices](https://docs.microsoft.com/aspnet/core/performance/performance-best-practices)

**Blazor WebAssembly Resources:**
- [Microsoft Blazor WebAssembly Debugging Guide](https://docs.microsoft.com/aspnet/core/blazor/debug)
- [Blazor WebAssembly Performance Best Practices](https://docs.microsoft.com/aspnet/core/blazor/webassembly-performance-best-practices)
- [Chrome WebAssembly Developer Tools](https://developer.chrome.com/docs/devtools/)

**General Resources:**
- [Visual Studio Code .NET Debugging](https://code.visualstudio.com/docs/languages/dotnet)
- [DotRush Extension Documentation](https://github.com/JaneySprings/DotRush)

## Conclusion

Syncfusion Code Studio delivers comprehensive debugging capabilities for modern web applications. The integrated DotRush extension enables efficient development workflows through advanced breakpoint management, variable inspection, and seamless code navigation.