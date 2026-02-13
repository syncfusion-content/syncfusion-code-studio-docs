---
title: How to resolve Code Studio app corruption
Description: Guide to fix application corruption on Windows and macOS.
platform: syncfusion-code-studio
keywords: cache, corruption, troubleshoot
---



# How to resolve Code Studio app corruption.

When Syncfusion Code Studio becomes corrupted or stops functioning correctly, a full reset of the application may be required. This guide provides detailed steps to completely remove Code Studio’s program files, configuration data, and related directories on both Windows and macOS. Performing this reset ensures that all corrupted components are cleared so you can reinstall and restore the application to a clean, stable state.

## Problem Summary

Application corruption can occur when essential Code Studio files—such as installation components, configuration data, or cache folders—become damaged or inconsistent. These issues may prevent the IDE from launching, updating, or functioning normally. This guide explains how to fully remove all relevant directories so that a clean reinstallation can rebuild fresh, working files and resolve corruption‑related problems.

## Possible Causes

- **Auto update issues**: Incomplete or interrupted automatic updates can sometimes affect application stability clearing the cache helps refresh the IDE and resolve update-related behavior.
- **System configuration updates**: Recent changes to your operating system settings may require a cache refresh to ensure compatibility.
- **Performance optimization**: Regularly clearing the cache helps maintain smooth and optimal application performance over time.

## Resolution Steps

### Step 1: Delete the Syncfusion Code Studio Folders

You need to delete the main application folders to completely resolve the issue.

#### Windows

Delete the Syncfusion Code Studio folders at these locations:

**Program Files:**
```
C:\Program Files\Syncfusion Code Studio
```
<img src="./troubleshoot-images/cache-image-programfiles.png" alt="cache">

**AppData Roaming:**
```
C:\Users\YourName\AppData\Roaming\Syncfusion Code Studio
```
<img src="./troubleshoot-images/cache-image-roaming.png" alt="cache">

#### macOS

Delete the Syncfusion Code Studio folders at these locations:

**Applications:**
```
/Applications/Syncfusion Code Studio
```
<img src="./troubleshoot-images/cache-image-macapplication.png" alt="cache">

**Application Support:**
```
/Users/YourName/Library/Application Support/Syncfusion Code Studio
```
<img src="./troubleshoot-images/cache-image-macroaming.png" alt="cache">



### Step 2: After Deleting Cache Folders

Once you've completed above step:

1. Restart your computer to ensure all files are properly released
2. Reinstall Syncfusion Code Studio, refer to the [Syncfusion Code Studio Install and Configure](/code-studio/getting-started/install-and-configuration) 
3. Launch the application - it will create fresh configuration files and cache

**Note:** Backup Recommendation - If you have custom configurations or settings you want to preserve, back up the relevant folders before deleting or clearing them.
