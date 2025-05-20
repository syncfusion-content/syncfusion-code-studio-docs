---
title: Rules
description: Details about configuring rules that define the behavior and constraints for language models in Cody IDE.
platform: syncfusion-cody
control: IDE
documentation: Getting Started
keywords: cody, IDE, installation, windows, setup, getting-started
---

# rules

A set of rules the LLM must follow, combined into the system message for every Chat, Edit, and Agent request.
Explicit rules can either be simple text or an object with the following 

## Properties:

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
    <td>A display name/title for the rule.</td>
  </tr>
  <tr>
    <td><code>rule</code></td>
    <td>Yes</td>
    <td>The text content of the rule.</td>
  </tr>
  <tr>
    <td><code>globs</code></td>
    <td>No</td>
    <td>
      When files are provided as context that match this glob pattern, the rule will be included.<br/>
      This can be either a single pattern (e.g., <code>"**/*.{ts,tsx}"</code>) or an array of patterns (e.g., <code>["src/**/*.ts", "tests/**/*.ts"]</code>).
    </td>
  </tr>
</table>

## Example:

{% tabs %}
{% highlight c# tabtitle="YAML" %}

rules:
  - Always annotate Python functions with their parameter and return types

  - name: TypeScript best practices
    rule: Always use TypeScript interfaces to define shape of objects. Use type aliases sparingly.
    globs: "**/*.{ts,tsx}"

  - name: TypeScript test patterns
    rule: In TypeScript tests, use Jest's describe/it pattern and follow best practices for mocking.
    globs:
      - "src/**/*.test.ts"
      - "tests/**/*.ts"

{% endhighlight %}
{% endtabs %}