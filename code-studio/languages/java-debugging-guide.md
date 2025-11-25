---
title: Setup and Debug Java Applications in Syncfusion Code Studio
description: Step-by-step guide to setup and debug Java applications using Syncfusion Code Studio's debugging features and tools.
platform: syncfusion-code-studio
control: IDE
documentation: Troubleshoot
keywords: java, jdk, maven, gradle, spring-boot, debug, debugging, breakpoints
---

# This Guide provides Step-By-Step Instructions for Setting-Up and Debugging Java Applications using Code Studio

## Language Setup

### Prerequisites

- Install the **Java Development Kit (JDK)** 8 or later from [Oracle JDK](https://www.oracle.com/java/technologies/downloads/) or [OpenJDK](https://openjdk.org/)
- Install **Maven** or **Gradle** build tools (optional, but recommended for project management)

### Verify Java Installation

Open the **Command Palette** (`Ctrl+Shift+P`)

Type `Java: Check Java Runtime` and select it

Verify that your JDK is detected and properly configured

## Required Extensions

To enable comprehensive Java debugging support, install the following extensions:

### Essential Extensions

**Extension Pack for Java**
- **Publisher**: Microsoft
- **Description**: Collection of extensions for Java development including Language Support for Java, Debugger for Java, Test Runner for Java, Maven for Java, and Visual Studio IntelliCode

The Extension Pack includes:

**Language Support for Java™** (by Red Hat)
- Java Linting, IntelliSense, formatting, refactoring, Maven/Gradle support

**Debugger for Java** (by Microsoft)
- Lightweight Java debugger with breakpoints, variable inspection, and call stack navigation

## Configuration Steps

### Step 1: Install Extensions

Open **Syncfusion Code Studio IDE**

Navigate to the **Extensions** view (`Ctrl+Shift+X`)

Search for "Extension Pack for Java"

Click **Install** on the Extension Pack for Java by Microsoft

Restart the IDE when prompted

### Step 2: Configure Java Environment

**Method 1: Using Settings**
- Open **Settings** (`Ctrl+,`)
- Search for "java.home"
- Set the path to your JDK installation

**Method 2: Using Environment Variable**
- Set `JAVA_HOME` environment variable to your JDK path
- Add `%JAVA_HOME%\bin` to your system PATH

### Step 3: Create Launch Configuration

Open your Java project in Syncfusion Code Studio IDE

Go to **Run and Debug** view (`Ctrl+Shift+D`)

Click **create a launch.json file**

Select **Java** environment

The IDE will create launch.json with basic configuration for debugging

## How to Run and Debug

Refer to [Common Debugging Steps](common-debugging-steps.md) for fundamental debugging procedures applicable to all languages.

### Language-Specific Debug Commands

**Java-Specific Methods**

**Using Command Palette**
- Open **Command Palette** (`Ctrl+Shift+P`)
- Type `Java: Debug`
- Select appropriate option

**Quick Debug**
- Open Java file with main method
- Press `F5` to debug current file

## Debugging Different Project Types

### Maven Projects

Ensure Maven extension is installed

Use Maven-specific launch configuration for proper classpath resolution

### Gradle Projects

Install Gradle for Java extension

Configure Gradle-specific settings for debugging

## Advanced Debugging Features

### Hot Code Replace

Enable automatic code replacement during debugging without restarting the session

### Exception Breakpoints

Set breakpoints that trigger when specific exceptions occur

Configure to break on caught or uncaught exceptions

## Unit Test Debugging

### Debug Single Test

Open test file

Click **Debug** above test method

Or use `Ctrl+F5` for quick test debugging

### Debug Test Suite

Right-click test class

Select **Debug Java** to run all tests in debug mode

## Troubleshooting Common Issues

### Issue 1: Debugger Not Starting

**Solutions:**
- Verify Java installation using `java -version`
- Check `java.home` setting in IDE preferences
- Restart IDE and clean workspace
- Rebuild project to ensure proper compilation

### Issue 2: Breakpoints Not Hit

**Solutions:**
- Ensure code is compiled with debug information
- Check if breakpoint is in executable code path
- Verify classpath configuration
- Clear workspace cache and rebuild

### Issue 3: Source Not Found

**Solutions:**
- Verify source paths are correctly configured
- Check Maven/Gradle source directory settings
- Ensure debug symbols are included in compilation

### Issue 4: Performance Issues

**Solutions:**
- Increase memory allocation for Java processes
- Disable unnecessary debugging features
- Use step filters to skip framework code
- Close unused debug sessions

