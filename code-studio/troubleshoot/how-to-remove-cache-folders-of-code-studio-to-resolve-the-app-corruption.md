---
title: How to remove cache folders of Code Studio to resolve app corruption
Description: Guide to delete Code Studio cache folders and config.yaml to fix application corruption on Windows and macOS.
platform: syncfusion-code-studio
keywords: cache, corruption, troubleshoot
---



# How to remove cache folders of Code Studio to resolve the app corruption.

This guide explains how to delete the Code Studio cache folders when you encounter application corruption issues.

## Problem Summary

This procedure helps you reset Syncfusion Code Studio to its default state by clearing cache files and configuration data. This process helps restore the application to its default state.

## Possible Causes

- **Auto update issues**: Incomplete or interrupted automatic updates can sometimes affect application stability clearing the cache helps refresh the IDE and resolve update-related behavior.
- **Configuration reset needed**: The `config.yaml` file may need to be restored to its default settings for the IDE to function correctly.
- **System configuration updates**: Recent changes to your operating system settings may require a cache refresh to ensure compatibility.
- **Performance optimization**: Regularly clearing the cache helps maintain smooth and optimal application performance over time.

## Resolution Steps

### Step 1: Delete the Syncfusion Code Studio Folders

After removing the configuration file, you need to delete the main application folders to completely clear the cache.

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

**Application Support:**
```
/Users/YourName/Library/Application Support/Syncfusion Code Studio
```
<img src="./troubleshoot-images/cache-image-macroaming.png" alt="cache">

**Applications:**
```
/Applications/Syncfusion Code Studio
```
<img src="./troubleshoot-images/cache-image-macapplication.png" alt="cache">

### Step 2: After Deleting Cache Folders

Once you've completed above step:

1. Restart your computer to ensure all files are properly released
2. Reinstall Syncfusion Code Studio, refer to the [Syncfusion Code Studio Install and Configure](/code-studio/getting-started/install-and-configuration) 
3. Launch the application - it will create fresh configuration files and cache

**Note:** Backup Recommendation - If you have custom configurations or settings you want to preserve, back up the relevant folders before deleting or clearing them.
