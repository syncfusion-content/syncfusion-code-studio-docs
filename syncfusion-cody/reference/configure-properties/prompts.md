---
title: "Prompts"
description: "Details about configuring custom prompts that can be used within Cody IDE."
platform: "syncfusion-cody"
control: "IDE"
documentation: "Getting Started"
keywords: "cody, IDE, installation, windows, setup, getting-started"
---

# prompts
A list of custom prompts that can be invoked from the chat window. Each prompt has a name, description, and the actual prompt text.

## Example


{% tabs %}
{% highlight c# tabtitle="YAML" %}

prompts:
  - name: check
    description: Check for mistakes in my code
    prompt: |
      Please read the highlighted code and check for any mistakes. You should look for the following, and be extremely vigilant:
        - Syntax errors
        - Logic errors
        - Security vulnerabilities

{% endhighlight %}
{% endtabs %}