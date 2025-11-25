---
title: Setup and Debug PHP Applications in Syncfusion Code Studio
description: Step-by-step guide to setup and debug PHP applications using Syncfusion Code Studio's debugging features and tools.
platform: syncfusion-code-studio
control: IDE
documentation: Troubleshoot
keywords: php, xdebug, debug, debugging, breakpoints
---

# This Guide provides Step-By-Step Instructions for Setting-Up and Debugging PHP Applications using Code Studio

## Language Setup

### Prerequisites

- Install **PHP** 8.3 or 8.4 from [windows.php.net](https://windows.php.net/download/) (Thread Safe version recommended)
- Install **Xdebug** extension for debugging support
- Configure system **PATH** environment variable

### Step-by-Step PHP Installation

#### 1. Download and Extract PHP

Download the **Thread Safe (TS)** ZIP package for Windows from [windows.php.net/download](https://windows.php.net/download/)

Extract the contents to a simple path like `C:\php`

**Note**: PHP 8.5 is not yet supported by Xdebug. Use PHP 8.3 or 8.4 for debugging support.

#### 2. Add PHP to System PATH

Press `Win + X` and select **System**

Click **Advanced system settings**

Click **Environment Variables**

Under **System variables**, find and select **Path**, then click **Edit**

Click **New** and add `C:\php`

Click **OK** on all dialogs to save changes

#### 3. Configure php.ini

Navigate to `C:\php` folder

Copy `php.ini-development` and rename the copy to `php.ini`

Open `php.ini` in a text editor

Enable essential extensions by removing the semicolon (;) at the beginning of these lines:
```ini
extension=curl
extension=mbstring
extension=openssl
extension=mysqli
extension=pdo_mysql
```

Save and close the file

#### 4. Verify PHP Installation

Open a **new** Command Prompt or PowerShell window

Run the following command:
```bash
php -v
```

You should see output showing the PHP version (e.g., PHP 8.3.x or 8.4.x)

### Step-by-Step Xdebug Installation

#### 1. Generate Xdebug Configuration

Open Command Prompt or PowerShell

Run the following command and save the output to a file:
```bash
php -i > phpinfo.txt
```

Open your web browser and navigate to [xdebug.org/wizard](https://xdebug.org/wizard)

Open `phpinfo.txt`, copy all contents, and paste into the Xdebug Wizard text box

Click **Analyse my phpinfo() output**

#### 2. Download Xdebug DLL

The wizard will show you specific instructions for your PHP version

Download the recommended Xdebug DLL file from the provided link

The file will be named something like `php_xdebug-3.x.x-8.3-ts-vs16-x86_64.dll`

#### 3. Install Xdebug Extension

Move the downloaded DLL file to `C:\php\ext\` directory

Rename the file to `php_xdebug.dll` for simplicity (optional but recommended)

Open `C:\php\php.ini` in a text editor

Scroll to the very end of the file and add the following configuration:
```ini
[xdebug]
zend_extension=xdebug
xdebug.mode=debug
xdebug.start_with_request=yes
xdebug.client_port=9003
xdebug.client_host=127.0.0.1
xdebug.log_level=0
```

Save the file

#### 4. Verify Xdebug Installation

Open a **new** Command Prompt or PowerShell window

Run the following command:
```bash
php -v
```

You should see output that includes:
```
PHP 8.x.x (cli) (built: ...)
...
with Xdebug v3.x.x, Copyright (c) 2002-2024, by Derick Rethans
```

Alternatively, run:
```bash
php -m
```

Look for `xdebug` in the list of loaded modules

If Xdebug is not showing, double-check your php.ini configuration and ensure the path to the DLL is correct

## Required Extensions

To enable comprehensive PHP debugging support, install the following extensions:

### Essential Extensions

**PHP Intelephense**
- **Publisher**: Ben Mewburn
- **Description**: High-performance PHP language support with IntelliSense, code navigation, formatting, and refactoring

**PHP Debug**
- **Publisher**: Xdebug
- **Description**: Debug support for PHP with Xdebug, providing breakpoints, step debugging, variable inspection, and call stack navigation
## Configuration Steps

### Step 1: Install Extensions

Open **Syncfusion Code Studio IDE**

Navigate to the **Extensions** view (`Ctrl+Shift+X`)

Search for "PHP Intelephense"

Click **Install** on the PHP Intelephense extension by Ben Mewburn

Search for "PHP Debug"

Click **Install** on the PHP Debug extension by Xdebug

Restart the IDE when prompted

### Step 2: Configure PHP Environment

**Method 1: Using Built-in PHP Server**
- Create or open a PHP project folder
- Open terminal in the IDE (`Ctrl+``)
- Navigate to your project root
- Start the built-in PHP server:
```bash
php -S localhost:8000
```
- Access your application at `http://localhost:8000`

**Method 2: Using External Web Server (Apache/Nginx)**
- Configure your web server to use the PHP installation
- Set document root to your project folder
- Ensure Xdebug is configured in `php.ini` as described in prerequisites
- Restart the web server after PHP configuration changes

**Method 3: Verify PHP Path in IDE**
- Open **Command Palette** (`Ctrl+Shift+P`)
- Type `Preferences: Open Settings (UI)`
- Search for `php.validate.executablePath`
- Set the path to your PHP executable (e.g., `C:\php\php.exe`)

### Step 3: Create Launch Configuration

Open your PHP project in Syncfusion Code Studio IDE

Go to **Run and Debug** view (`Ctrl+Shift+D`)

Click **create a launch.json file**

Select **PHP** environment

The IDE will create `.vscode/launch.json` with basic configuration for debugging

## How to Run and Debug

Refer to [Common Debugging Steps](common-debugging-steps.md) for fundamental debugging procedures applicable to all languages.

### Language-Specific Debug Commands and Features

**PHP-Specific Breakpoint Methods**
- **Function Breakpoints**: Set breakpoints on specific PHP function calls

**PHP-Specific Debug Methods**

**Method 1: Debug Current Script**
- Open a PHP file in the editor
- Set breakpoints by clicking in the gutter (left of line numbers)
- Open **Run and Debug** view (`Ctrl+Shift+D`)
- Select **Launch currently open script** from dropdown
- Click **Start Debugging** (`F5`) or press `F5`
- Script executes with debugger attached

**Method 2: Debug Web Application (Listen Mode)**
- Open **Run and Debug** view (`Ctrl+Shift+D`)
- Select **Listen for Xdebug** from dropdown
- Click **Start Debugging** (`F5`)
- The debugger will wait for incoming connections
- Open your web browser and navigate to your application (e.g., `http://localhost:8000`)
- Xdebug will connect automatically when PHP script executes
- Execution will pause at breakpoints

**Method 3: Debug with Built-in Server**
- Open **Run and Debug** view (`Ctrl+Shift+D`)
- Select **Launch Built-in web server** from dropdown
- Click **Start Debugging** (`F5`)
- The PHP built-in server starts automatically
- Browser opens automatically to your application
- Set breakpoints and interact with your application

**Method 4: Using Command Palette**
- Open **Command Palette** (`Ctrl+Shift+P`)
- Type `Debug: Start Debugging`
- Select appropriate PHP debug configuration

## Debugging Different Project Types

### Standard PHP Scripts

Use **Launch currently open script** configuration

Ideal for CLI scripts, cron jobs, and standalone PHP files

### Web Applications (Plain PHP)

Use **Listen for Xdebug** or **Launch Built-in web server** configuration

Set breakpoints in PHP files that handle web requests

Test application through browser while debugger is listening

Use **Launch Built-in web server** with appropriate document root

Set `cwd` in launch.json to project root directory

### Laravel Applications

Use **Listen for Xdebug** configuration

Start Laravel development server: `php artisan serve`

Set breakpoints in controllers, models, or middleware

Access application through browser at `http://localhost:8000`

### WordPress Development

Configure web server (Apache/Nginx) to serve WordPress

Use **Listen for Xdebug** configuration

Start debugging session before accessing WordPress admin or frontend

Set breakpoints in themes, plugins, or core files

### API Development

Use **Listen for Xdebug** configuration

Test API endpoints using tools like Postman or cURL

Debugger catches requests and pauses at breakpoints

Inspect request data, headers, and response generation

## Advanced Debugging Features

### Path Mapping (Remote Debugging)

Configure path mappings for debugging applications on remote servers

Map remote file paths to local workspace paths

Useful for Docker containers, virtual machines, or remote servers

### Multi-session Debugging

Enable debugging of multiple PHP processes simultaneously

Each session appears separately in **Call Stack** panel

Useful for debugging AJAX requests or background processes

### Xdebug Profiling

Enable profiling mode to analyze performance

Add to php.ini:
```ini
xdebug.mode=debug,profile
xdebug.output_dir="/tmp/xdebug"
```

Analyze generated cachegrind files with tools like KCachegrind or Webgrind

### Step Filtering

Configure step filters to skip debugging vendor code or specific files

Improves debugging performance for large projects

## Unit Test Debugging

### Debugging Specific Test

Open the test file in editor

Set breakpoints in test methods

Press `F5` to debug current test file

Inspect variables, assertions, and test data during execution

## Troubleshooting Common Issues

### Issue 1: Debugger Not Starting

**Solutions:**
- Verify PHP installation: run `php -v` in terminal
- Verify Xdebug installation: run `php -m` and look for `xdebug`
- Check `php.ini` has correct Xdebug configuration
- Ensure `xdebug.mode=debug` is set in php.ini
- Restart IDE after changing php.ini
- Check PHP Debug extension is installed and enabled
- Verify port 9003 is not blocked by firewall

### Issue 2: Breakpoints Not Hit

**Solutions:**
- Ensure Xdebug is properly installed (check `php -v` output)
- Verify `xdebug.start_with_request=yes` is set in php.ini
- Check that breakpoints are set on executable PHP code (not comments or blank lines)
- Ensure the correct PHP file is being executed
- Verify path mappings if using remote debugging
- Check Xdebug log for connection issues (set `xdebug.log` in php.ini)
- Try restarting the debug session

### Issue 3: "Connection Timeout" Error

**Solutions:**
- Verify Xdebug is configured to connect to correct host and port
- Check firewall settings allow connections on port 9003
- Ensure IDE is listening for Xdebug connections before running script
- Verify `xdebug.client_host=127.0.0.1` in php.ini
- Check if another debugger is using port 9003
- Try changing Xdebug port in both php.ini and launch.json

### Issue 4: "Source Not Found" Error

**Solutions:**
- Verify PHP source files are in the workspace folder
- Check path mappings configuration for remote/Docker debugging
- Ensure file paths in launch.json are correct
- Verify workspace folder is correctly opened in IDE
- Check that symlinks are properly resolved

### Issue 5: Xdebug Not Loading

**Solutions:**
- Verify Xdebug DLL file exists in `C:\php\ext\` directory
- Check that `zend_extension=xdebug` line in php.ini has correct path
- Ensure you're using Thread Safe (TS) PHP with matching Xdebug version
- Verify PHP version matches Xdebug version (use Xdebug wizard)
- Check php.ini file is in correct location (run `php --ini`)
- Look for PHP errors when running `php -v`

### Issue 6: Performance Issues During Debugging

**Solutions:**
- Disable Xdebug when not debugging (comment out zend_extension line)
- Use conditional breakpoints instead of many regular breakpoints
- Reduce the number of watch expressions
- Avoid hovering over large arrays or objects
- Increase PHP memory limit if needed (`memory_limit` in php.ini)
- Close unused debug sessions
- Use step filters to skip vendor code

### Issue 7: PHP Built-in Server Not Starting

**Solutions:**
- Verify port 8000 (or configured port) is not already in use
- Check that PHP CLI is working: `php -v`
- Ensure current working directory (`cwd`) in launch.json is correct
- Verify no other web server is running on the same port
- Check terminal output for PHP errors
- Try different port number in launch configuration

### Issue 8: Variables Not Showing in Debug Panel

**Solutions:**
- Ensure execution has hit a breakpoint
- Check that Xdebug is properly connected (look for "Listening..." in status bar)
- Verify variables are in current scope
- Try expanding variable sections (VARIABLES, WATCH, CALL STACK)
- Check Xdebug configuration has `xdebug.mode=debug`
- Restart debugging session
- Check for Xdebug version compatibility issues

## Best Practices

### Development Workflow

Always use virtual hosts or the built-in PHP server for local development

Keep Xdebug disabled in production environments (performance impact)

Use version control (Git) to track launch.json configurations

Organize projects with clear folder structure

### Security Considerations

Never commit php.ini with sensitive information to version control

Restrict Xdebug to local connections only (`xdebug.client_host=127.0.0.1`)

Disable Xdebug on production servers

Use strong passwords for any remote debugging scenarios

### Performance Tips

Only enable Xdebug when actively debugging

Use conditional breakpoints to reduce debugging overhead

Profile specific code sections rather than entire application

Implement proper caching strategies in development

### Code Quality

Use PHP CodeSniffer for code style enforcement

Integrate PHPStan or Psalm for static analysis

Write unit tests alongside debugging sessions

Document complex debugging scenarios in code comments