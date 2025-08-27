---
title: "Syncfusion Code Studio Custom Prompts"
description: "Guide for creating and using AI-driven prompt templates to standardize development workflows"
platform: syncfusion-code-studio
keywords: custom-prompts, ai-assistance, templates, workflows, best-practices
---

# Custom Prompts

Custom prompts let you encode your team’s coding standards into reusable templates. This delivers consistent, high-quality AI assistance and speeds up routine tasks.

## Purpose

The primary purpose of custom prompts is to streamline and standardize development workflows by:

- **Enforcing Best Practices**: Ensure generated code adheres to team conventions.
- **Improving Consistency**: Standardize how common tasks are performed.
- **Accelerating Development**: Automate repetitive coding tasks with predefined templates.
 

## Prompt File Structure 

- **name**: Unique identifier (e.g., GenerateTestCases)
- **description**: Short summary of intent
- **prompt**: Literal instructions (role, tasks, output format)

## How to use Prompt Files 
 
1. Click the “Add Prompt” button, Code Studio will automatically generate your new prompt file under the `sfcodestudio/prompts/` directory. 
2. In Code Studio chat, type `/` and pick your prompt.  
3. Highlight code or supply context.  
4. Run the prompt and review suggestions.  
5. Apply accepted changes via IDE refactoring tools.  

<img src="../reference-images/prompt.gif" alt="Prompt" >

## Example Prompt

```yaml
name: GenerateTestCases
description: Generate test cases for the current application
prompt:
    1. Identify key functionalities to test based on user stories and requirements
    2. Use best practices and test design techniques for each test case
    3. Write testable code for each test case using popular testing frameworks
    4. Verify the return values and edge cases for each test case
    5. Document test cases and set test coverage for each functionality
  ```




