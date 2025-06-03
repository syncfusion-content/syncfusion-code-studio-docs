---
title: docs
description: Details about configuring documentation sources to be indexed and made available for Syncfusion code studio IDE's language models.
platform: syncfusion-code-studio
control: IDE
documentation: Getting Started
keywords: code, IDE, installation, windows, setup, getting-started
---

# docs

List of documentation sites to index.

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
    <td>Name of the documentation site, displayed in dropdowns, etc.</td>
  </tr>
  <tr>
    <td><code>startUrl</code></td>
    <td>Yes</td>
    <td>Start page for crawling – usually the root or intro page for docs.</td>
  </tr>
  <tr>
    <td><code>maxDepth</code></td>
    <td>No</td>
    <td>Maximum link depth for crawling. Default is 4.</td>
  </tr>
  <tr>
    <td><code>favicon</code></td>
    <td>No</td>
    <td>URL for site favicon (default is <code>/favicon.ico</code> from <code>startUrl</code>).</td>
  </tr>
  <tr>
    <td><code>useLocalCrawling</code></td>
    <td>No</td>
    <td>Skip the default crawler and only crawl using a local crawler.</td>
  </tr>
</table>

## Example


```yaml
docs:
  - name: Syncfusion PDF
    startUrl: https://help.syncfusion.com/file-formats/pdf/working-with-document
```