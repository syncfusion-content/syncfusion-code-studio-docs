# Ruby Development and Debugging Setup Guide for Code stduio

This comprehensive guide will help you set up Ruby development and debugging in Code Stduio on Windows.

## Prerequisites

### 1. Install Ruby
- Download Ruby from [rubyinstaller.org](https://rubyinstaller.org/)
- Choose Ruby+Devkit version (recommended: Ruby 3.1 or higher)
- During installation, make sure to check "Add Ruby executables to your PATH"
- Install MSYS2 development toolchain when prompted

### 2. Verify Ruby Installation
Open PowerShell and run:
```powershell
ruby --version
gem --version
```

## VS Code Extensions Setup

### Required Extensions

1. **Shopify Ruby LSP** (Recommended)
   - Extension ID: `Shopify.ruby-lsp`
   - Provides modern Ruby language support with debugging

2. **Ruby Debug** (Alternative)
   - Extension ID: `castwide.ruby-debug`
   - Traditional Ruby debugger

### Installation Steps

1. Open VS Code
2. Go to Extensions (Ctrl+Shift+X)
3. Search for "Ruby LSP" and install the Shopify Ruby LSP extension
4. Restart VS Code

## Required Ruby Gems

Install the necessary debugging gems:

```powershell
# For Ruby LSP debugging
gem install debug

# For traditional ruby-debug (if using castwide.ruby-debug)
gem install ruby-debug-ide debase
```

## VS Code Configuration

### 1. Create Launch Configuration

Create `.vscode/launch.json` in your project folder:

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Debug Current Ruby File",
            "type": "ruby",
            "request": "launch",
            "program": "${file}",
            "cwd": "${workspaceFolder}",
            "args": []
        },
        {
            "name": "Debug hello_world.rb",
            "type": "ruby",
            "request": "launch",
            "program": "${workspaceFolder}/hello_world.rb",
            "cwd": "${workspaceFolder}",
            "args": []
        }
    ]
}
```

### 2. Workspace Settings (Optional)

Create `.vscode/settings.json`:

```json
{
    "ruby.format": "rubocop",
    "ruby.lint": {
        "rubocop": true
    },
    "ruby.useLanguageServer": true
}
```

## Debugging Your Ruby Code

### Method 1: Using Breakpoints (Recommended)

1. Open your Ruby file in VS Code
2. Click on the line number where you want to set a breakpoint (red dot appears)
3. Press `F5` or go to Run and Debug panel
4. Select your debug configuration
5. Your code will pause at the breakpoint

### Method 2: Using debugger Statement

Add `debugger` statements in your code:

```ruby
require 'debug'

def calculate(x, y)
    debugger  # Execution will pause here
    result = x + y
    result
end

puts calculate(5, 3)
```

### Method 3: Command Line Debugging

For troubleshooting, you can debug from terminal:

```powershell
# Using built-in debug library
ruby -r debug your_file.rb

# Using traditional debugger (if installed)
rdebug your_file.rb
```

## Common Issues and Solutions

### Issue 1: "debug gem version less than 1.8.0"

**Solution:**
```powershell
gem update debug
gem install debug --version "~> 1.8"
```

### Issue 2: "rdbg command not found"

**Solution:**
```powershell
# Uninstall problematic rdbg extension
# Install Shopify Ruby LSP instead
gem install debug
```

### Issue 3: "Native extension build failed"

**Solution:**
1. Install Ruby+Devkit version
2. Install MSYS2 development tools
3. Or use pre-compiled gems:
```powershell
gem install debug --platform ruby
```

### Issue 4: Breakpoints not working

**Solutions:**
- Ensure you're using the correct debug configuration type
- Check that the Ruby file is saved
- Verify the Ruby extension is active (check status bar)
- Try adding `require 'debug'` at the top of your file

## Testing Your Setup

### 1. Create a Test File

Create `debug_test.rb`:

```ruby
require 'debug'

puts "Starting debug test..."

# Variables to inspect
x = 10
y = 20

# This line should trigger breakpoint when debugging
result = x + y  # Set breakpoint here

puts "Result: #{result}"

# Test with methods
def greet(name)
    message = "Hello, #{name}!"  # Set another breakpoint here
    puts message
end

greet("Ruby Developer")

puts "Debug test completed!"
```

### 2. Debug the Test File

1. Open `debug_test.rb` in VS Code
2. Set breakpoints on lines with `result = x + y` and `message = "Hello, #{name}!"`
3. Press `F5` to start debugging
4. Use the debug panel to:
   - Step over (`F10`)
   - Step into (`F11`)
   - Continue (`F5`)
   - Inspect variables in the Variables panel

## Debug Panel Features

When debugging, you'll see:

- **Variables**: Current variable values
- **Watch**: Custom expressions to monitor
- **Call Stack**: Function call hierarchy
- **Breakpoints**: Manage all breakpoints

### Debug Controls

- **Continue (F5)**: Resume execution
- **Step Over (F10)**: Execute current line
- **Step Into (F11)**: Enter function calls
- **Step Out (Shift+F11)**: Exit current function
- **Restart (Ctrl+Shift+F5)**: Restart debugging
- **Stop (Shift+F5)**: Stop debugging

## Best Practices

1. **Use meaningful variable names** for easier debugging
2. **Set breakpoints at key decision points** in your code
3. **Use the watch panel** to monitor specific expressions
4. **Step through code methodically** rather than just continuing
5. **Remove debugger statements** before committing code

## Troubleshooting Checklist

- [ ] Ruby is installed and in PATH
- [ ] Required gems are installed (`debug`, `ruby-debug-ide`, `debase`)
- [ ] VS Code Ruby extension is installed and enabled
- [ ] Launch configuration is properly set up
- [ ] File is saved before debugging
- [ ] Breakpoints are set on executable lines (not comments/blank lines)

## Additional Resources

- [Ruby LSP Documentation](https://shopify.github.io/ruby-lsp/)
- [VS Code Ruby Debugging Guide](https://code.visualstudio.com/docs/languages/ruby)
- [Ruby Debug Gem Documentation](https://github.com/ruby/debug)

## Example Project Structure

```
your-ruby-project/
├── .vscode/
│   ├── launch.json
├── lib/
│   └── your_classes.rb
├── test/
├── hello_world.rb
└── debug_test.rb
```

---

## Quick Start Checklist

1. ✅ Install Ruby+Devkit
2. ✅ Install Code stdui Shopify Ruby LSP extension  
3. ✅ Run `gem install debug`
4. ✅ Create `.vscode/launch.json` with proper configuration
5. ✅ Set breakpoints in your Ruby file
6. ✅ Press F5 to start debugging
7. ✅ Use debug controls to step through code