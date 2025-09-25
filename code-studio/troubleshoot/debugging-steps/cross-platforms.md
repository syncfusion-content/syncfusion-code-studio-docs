---
title: Run and Debug Flutter Application in Syncfusion Code Studio
description: Step-by-step guide to run and debug application in Flutter Platforms using Syncfusion Code Studio's debugging features and tools.
platform: syncfusion-code-studio
control: IDE
documentation: Troubleshoot
keywords: flutter, desktop, android, ios, mac, web, debug, debugging, breakpoints, step-through, variables, watch, call-stack, output, troubleshoot, code-studio
---

# This guide provides step-by-step instructions for debugging a Flutter application using Code Studio

## Prerequisites

**Install Flutter SDK:**

- Windows:

    - Download the Flutter SDK from https://docs.flutter.dev/install/manual

    - Select Windows and Download the zip file.

    - Extract the zip file to a location like `C:flutter\src\`

    - Add Flutter to your PATH:

    - Search for "Environment Variables" in Windows search

    - Click "Environment Variables"

    - Under "User variables", find PATH and click "Edit"

    - Click "New" and add the full path to `flutter\bin`

    - Click "OK" to save

- macOS:

    - Follow the instruction from https://docs.flutter.dev/get-started/install/macos 

- Linux:
    - Follow the instruction from https://docs.flutter.dev/get-started/install/linux 

 

## Steps to Run and Debug a Flutter Application in Code Studio

### Step 1: Create a Flutter Project
- Create a New Flutter Project:
Open a terminal (e.g., Command Prompt, PowerShell, or Code Studio’s integrated terminal). 
`flutter create MyFlutterApp`

- Navigate to the project folder: `cd MyFlutterApp`

### Step 2: Running the Application
#### For Windows:

- To deploy the Flutter application on Windows by running this command: `flutter run -d windows`

#### For Android:

- Check available emulators by running this command: `flutter emulators`

- To open the emulator, run this command: `flutter emulators --launch pixel_7_-_api_35`

- To deploy the Flutter application on Android by running this command: `flutter run`

#### For Web:

- To deploy the Flutter application on the Web by running this command: `flutter run`

#### For macOS:

- To deploy the Flutter application on macOS by running this command: `flutter run -d macos`

#### For iOS:

- Open the simulator on macOS.

- To deploy the Flutter application on iOS by running this command: `flutter run`

Run the commands in the Code Studio terminal.

 
 
## Quick Commands Reference 
```bash
# Essential Commands
flutter doctor              # Check your setup
flutter devices             # See available devices
flutter create my_app       # Create new project
flutter run                 # Run your app
flutter build apk --release # Build Android APK
flutter build web --release # Build for web


# Troubleshooting
flutter clean               # Clean build files
flutter pub get             # Get dependencies
```