---
title: "Models"
description: "Details about configuring language models that are available for use in Cody IDE."
platform: "syncfusion-cody"
control: "IDE"
documentation: "Getting Started"
keywords: "cody, IDE, installation, windows, setup, getting-started"
---

# models

The `models` section specifies the language models included in your configuration. These models power features like chat, editing, and summarization.

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
    <td>A unique name to identify the model within your configuration.</td>
  </tr>
  <tr>
    <td><code>provider</code></td>
    <td>Yes</td>
    <td>The provider of the model (e.g., openai, ollama).</td>
  </tr>
  <tr>
    <td><code>model</code></td>
    <td>Yes</td>
    <td>The specific model name (e.g., gpt-4, starcoder).</td>
  </tr>
  <tr>
    <td><code>apiBase</code></td>
    <td>No</td>
    <td>Can be used to override the default API base that is specified per model.</td>
  </tr>
  <tr>
    <td><code>roles</code></td>
    <td>No</td>
    <td>An array specifying the roles this model can fulfill, such as chat, autocomplete, embed, rerank, edit, apply.</td>
  </tr>
  <tr>
    <td><code>capabilities</code></td>
    <td>No</td>
    <td>
      An array of strings that specify the model's capabilities, overriding Cody's automatic detection based on the provider and model.<br/>
      Supported capabilities include <code>tool_use</code> and <code>image_input</code>.
    </td>
  </tr>
  <tr>
    <td><code>embedOptions</code></td>
    <td>No</td>
    <td>
      If the model includes role <code>embed</code>, these settings apply for embeddings:<br/><br/>
      - <code>maxChunkSize</code>: Maximum tokens per document chunk. Minimum is 128 tokens.<br/>
      - <code>maxBatchSize</code>: Maximum number of chunks per request. Minimum is 1 chunk.
    </td>
  </tr>
  <tr>
    <td><code>defaultCompletionOptions</code></td>
    <td>No</td>
    <td>
      Default completion options for model settings:<br/><br/>
      - <code>contextLength</code>: Maximum context length of the model, typically in tokens.<br/>
      - <code>maxTokens</code>: Maximum number of tokens to generate in a completion.<br/>
      - <code>temperature</code>: Controls the randomness of the completion. Values range from 0.0 (deterministic) to 1.0 (random).<br/>
      - <code>topP</code>: The cumulative probability for nucleus sampling.<br/>
      - <code>topK</code>: Maximum number of tokens considered at each step.<br/>
      - <code>stop</code>: An array of stop tokens that will terminate the completion.<br/>
      - <code>reasoning</code>: Boolean to enable thinking/reasoning for Anthropic Claude 3.7+ models.<br/>
      - <code>reasoningBudgetTokens</code>: Budget tokens for thinking/reasoning in Anthropic Claude 3.7+ models.
    </td>
  </tr>
</table>

## Example

{% tabs %}
{% highlight c# tabtitle="YAML" %}

name: Local Assistant
version: 1.0.0
schema: v1
models:
  - name: GPT-4o
    provider: openai
    model: gpt-4o
    roles:
      - chat
      - edit
      - apply
    defaultCompletionOptions:
      temperature: 0.7
      maxTokens: 1500

  - name: Codestral
    provider: mistral
    model: codestral-latest
    roles:
      - autocomplete

  - name: My Model - OpenAI-Compatible
    provider: openai
    apiBase: http://my-endpoint/v1
    model: my-custom-model
    capabilities:
      - tool_use
      - image_input
    roles:
      - chat
      - edit

{% endhighlight %}
{% endtabs %}