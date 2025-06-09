---
title: Mcp Server
description: Details about configuring MCP (Model Context Protocol) servers that can be used as context providers in Syncfusion code studio IDE.
platform: syncfusion-code-studio
control: IDE
documentation: Getting Started
keywords: code, IDE, installation, windows, setup, getting-started
---

# MCP Servers

The Model Context Protocol is a standard proposed by Anthropic to unify prompts, context, and tool use. Syncfusion code studio supports any MCP server with the MCP context provider.

## Properties

<table>
  <thead>
    <tr>
      <th>Property</th>
      <th>Is Required</th>
      <th>Description</th>
    </tr>
  </thead>
  <tr>
    <td><code>name</code></td>
    <td>Yes</td>
    <td>The name of the MCP server.</td>
  </tr>
  <tr>
    <td><code>command</code></td>
    <td>Yes</td>
    <td>The command used to start the server.</td>
  </tr>
  <tr>
    <td><code>args</code></td>
    <td>No</td>
    <td>An optional array of arguments for the command.</td>
  </tr>
  <tr>
    <td><code>env</code></td>
    <td>No</td>
    <td>An optional map of environment variables for the server process.</td>
  </tr>
  <tr>
    <td><code>connectionTimeout</code></td>
    <td>No</td>
    <td>An optional connection timeout number to the server in milliseconds.</td>
  </tr>
</table>


## Example

```yaml
mcpServers:
  - name: My MCP Server
    command: uvx
    args:
      - mcp-server-sqlite
      - --db-path
      - /Users/NAME/test.db
 ```     
