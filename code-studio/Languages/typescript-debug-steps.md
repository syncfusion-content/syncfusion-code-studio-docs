---
title: "Syncfusion Code Studio Languages"
description: "Professional guide for TypeScript development and debugging setup in Code Studio"
classification: "User Guide - Troubleshoot"
platform: syncfusion-code-studio
keywords: TypeScript, debugging, development, troubleshoot, code-studio, syncfusion
---

# TypeScript Development and Debugging Setup Guide for Code Studio

This comprehensive guide will help you set up TypeScript development and debugging in Code Studio.

## Prerequisites

Before setting up TypeScript development in Code Studio, ensure you have the following prerequisites:

### 1. Install Node.js and npm
1. Download Node.js from [nodejs.org](https://nodejs.org/downloads/)
2. Choose **LTS version** (recommended: Node.js 18 or higher)
3. During installation:
   - Accept the default installation directory
   - Check "Automatically install the necessary tools" if prompted

### 2. Verify Node.js and npm Installation
Open PowerShell as Administrator and run the following commands:
```powershell
node --version
npm --version
```

If any command fails or shows an error, restart your terminal or computer and try again.

### 3. Install TypeScript Globally (Optional but Recommended)
Open PowerShell as Administrator and execute the following command:
```powershell
# Install TypeScript compiler globally
npm install -g typescript

# Install ts-node for direct TypeScript execution (optional)
npm install -g ts-node
```

## Required Node.js Packages

For TypeScript development, install the following packages in your project:

```powershell
# Navigate to your project directory
cd your-project-directory

# Initialize npm project if not already done
npm init -y

# Install TypeScript as development dependency
npm install --save-dev typescript @types/node

# Install ts-node for direct execution (optional)
npm install --save-dev ts-node

# Create TypeScript configuration file
npx tsc --init
```

## Working with TypeScript Projects

### Opening TypeScript Development Projects

Once you have completed the setup, you can start working with TypeScript projects in Code Studio:

#### 1. Open a TypeScript Project
Use one of the following methods to open your TypeScript project:
- **File Menu**: Go to `File > Open Folder` and select your TypeScript project directory
- **Command Palette**: Press `Ctrl+Shift+P`, type "Open Folder", and select your project directory
- **Drag and Drop**: Drag your project folder directly into Code Studio

### Running TypeScript Projects

#### Using Code Studio Run Features
1. **Compile and Run TypeScript File**:
   - Open your TypeScript file (`.ts`)
   - Press `Ctrl+F5` to run without debugging
   - Alternatively, right-click in the editor and select "Run Code"

#### Using Terminal Execution
1. **Open Integrated Terminal**:
   - Press `Ctrl+`` (backtick) to open the terminal
   - Navigate to your project directory if needed
   
2. **Compile and Run the TypeScript File**:
   ```powershell
   # Method 1: Compile then run
   tsc filename.ts
   node filename.js
   
   # Method 2: Direct execution with ts-node (if installed)
   ts-node filename.ts
   
   # Method 3: Using npm scripts (if configured in package.json)
   npm run build
   npm start
   ```

### Debugging TypeScript Projects

#### Quick Debug
1. **Debug TypeScript File Directly**:
   - Open your TypeScript file (`.ts`)
   - Press `F5` to run with debugging
   - Alternatively, right-click in the editor and select "Debug TypeScript File"

#### Using Debug Panel
1. **Set Up Debug Configuration**:
   - Open Run and Debug view (`Ctrl+Shift+D`)
   - Click the "Run and Debug" button
   - Click the "create a launch.json file" link
   - Select "Node.js" from the dropdown menu
   - Choose the "Launch Program" option
   
2. **Configure for TypeScript**:
   - Update the `launch.json` configuration for Chrome debugging with source map support:
   ```json
   {
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Debug TypeScript App",
            "type": "chrome",
            "request": "launch",
            "url": "http://localhost:3000",
            "webRoot": "${workspaceFolder}",
            "sourceMaps": true,
            "sourceMapPathOverrides": {
                "webpack:///./src/*": "${webRoot}/src/*",
                "webpack://ej2-quickstart/./src/*": "${webRoot}/src/*",
                "webpack:///src/*": "${webRoot}/src/*",
                "webpack:///*": "*"
            },
            "skipFiles": [
                "${workspaceFolder}/node_modules/**/*.js",
                "<node_internals>/**/*.js"
            ]
        }
    ]
   }
   ```
   
3. **Launch Debug Session**:
   - Code Studio will execute your TypeScript file with debugging capabilities
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
- **Debug Console**: Evaluate TypeScript/JavaScript expressions during debugging
- **Call Stack**: View the current execution stack

## Troubleshooting

### Common Issues and Solutions

#### 1. TypeScript Not Recognized in Terminal
**Problem**: When running `tsc --version`, you get "'tsc' is not recognized as an internal or external command"

**Solutions**:
- Restart Code Studio and your computer after Node.js installation
- Install TypeScript globally: `npm install -g typescript`
- Use npx to run the TypeScript compiler: `npx tsc --version`
- Verify Node.js and npm are installed and in PATH:
  ```powershell
  # Check if Node.js is in PATH
  echo $env:PATH
  
  # Check npm global packages location
  npm config get prefix
  ```
- Add npm global packages to PATH if needed

#### 2. Debug Session Won't Start
**Problem**: Clicking F5 or "Run and Debug" doesn't start debugging session

**Solutions**:
- Install the required packages: `npm install --save-dev ts-node @types/node`
- Verify that Code Studio's JavaScript debugger is enabled
- Check that the `launch.json` configuration is correct
- Ensure that `tsconfig.json` exists in your project root
- Try creating a new `launch.json` file:
  - Open Run and Debug view (`Ctrl+Shift+D`)
  - Click "create a launch.json file"
  - Select "Node.js"
- Restart Code Studio after installing packages

#### 3. Breakpoints Not Working
**Problem**: Breakpoints are set but debugger doesn't stop at them

**Solutions**:
- Ensure you're running with debugging (`F5`) and not just running (`Ctrl+F5`)
- Verify that source maps are enabled in `tsconfig.json`:
  ```json
  {
    "compilerOptions": {
      "sourceMap": true,
      "inlineSourceMap": false
    }
  }
  ```
- Verify breakpoints are set on executable lines (not comments, empty lines, or type definitions)
- Make sure your TypeScript file is saved before debugging
- Clear compiled JavaScript files and rebuild: `npx tsc --build --clean`
- Reload the window: Press `Ctrl+Shift+P` and type "Developer: Reload Window"

#### 4. Module Import Errors
**Problem**: TypeScript shows import errors or cannot find modules

**Solutions**:
- Install the required type definitions: `npm install --save-dev @types/node @types/module-name`
- Verify the `tsconfig.json` module resolution settings:
  ```json
  {
    "compilerOptions": {
      "moduleResolution": "node",
      "esModuleInterop": true,
      "allowSyntheticDefaultImports": true
    }
  }
  ```
- Verify package is installed: `npm list package-name`
- Use TypeScript Importer extension for auto-import suggestions

#### 5. Webpack Configuration for TypeScript Development
**Problem**: Need to set up Webpack for TypeScript projects with proper debugging support

**Solutions**:
- Install the required Webpack packages:
  ```powershell
  npm install --save-dev webpack webpack-cli webpack-dev-server ts-loader
  ```
- Create or update a `webpack.config.js` file in your project root with debugging-optimized settings:
  ```javascript
  module.exports = {
      mode: 'development',
      devtool: 'source-map',
      entry: './src/app.ts',
      output: {
          filename: 'bundle.js',
          path: __dirname + '/dist',
          publicPath: '/dist/'
      },
      resolve: {
          extensions: ['.ts', '.js']
      },
      module: {
          rules: [
              {
                  test: /\.ts$/,
                  use: 'ts-loader',
                  exclude: /node_modules/
              }
          ]
      },
      devServer: {
          static: './',
          port: 3000,
          hot: true
      }
  };
  ```
- Add npm scripts to your `package.json`:
  ```json
  {
    "scripts": {
      "build": "webpack",
      "dev": "webpack serve --open",
      "watch": "webpack --watch"
    }
  }
  ```