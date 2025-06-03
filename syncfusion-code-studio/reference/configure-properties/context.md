---
title: context
description: Details about configuring context providers that supply additional information to language models in Syncfusion code studio IDE.
platform: syncfusion-code-studio
control: IDE
documentation: Getting Started
keywords: code, IDE, installation, windows, setup, getting-started
---
# context

The context section specifies context providers that deliver extra information to the language models. Each provider can be customized with its own set of parameters

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
    <td><code>provider</code></td>
    <td>Yes</td>
    <td>The identifier or name of the context provider (e.g., code, docs, web).</td>
  </tr>
  <tr>
    <td><code>name</code></td>
    <td>No</td>
    <td>Optional name for the provider.</td>
  </tr>
  <tr>
    <td><code>params</code></td>
    <td>No</td>
    <td>Optional parameters to configure the context provider's behavior.</td>
  </tr>
</table>

## Add the context provider in the config.yaml file as follows

```yaml
context:
  - provider: file
  - provider: code
  - provider: codebase
    params:
      nFinal: 10
  - provider: docs
  - provider: diff
  - provider: http
    name: Context Server 1
    params:
      url: "https://api.example.com/server1"
  - provider: folder
  - provider: terminal
```
