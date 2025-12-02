

# Debugging in Action

## Debug Process Walkthrough

<img src="desktop-images/debug-app.gif" alt="Debug Process Demonstration">

The above animation demonstrates the complete debugging workflow from setting breakpoints to hitting them during execution.

The application will launch, and the debugger will attach. If a breakpoint is hit, execution pauses, and you can inspect variables in the Debug panel (Variables, Call Stack, or Watch windows).

# Debugging Features Reference

| Feature          | Shortcut        | Description                                                 |
|------------------|----------------|-------------------------------------------------------------|
| **Step Into**    | `F11`           | Step into a method call to debug inside the method           |
| **Step Over**    | `F10`           | Execute the current line without stepping into method calls  |
| **Step Out**     | `Shift+F11`     | Exit the current method and return to the caller             |
| **Continue**     | `F5`            | Resume execution until the next breakpoint                   |
| **Restart**      | `Ctrl+Shift+F5` | Restart the debugging session                                |
| **Stop**         | `Shift+F5`      | Stop the debugging session                                   |

## Platform Consistency

**Important:** These debugging features, keyboard shortcuts, and debugging interface work identically across:

- WinForms applications
- WPF applications
- WinUI applications

The underlying .NET debugging experience in Syncfusion Code Studio remains consistent regardless of the desktop UI framework you're using.
