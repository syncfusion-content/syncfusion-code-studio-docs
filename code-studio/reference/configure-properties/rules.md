---
title: Rules
description: Details about configuring rules that define the behavior and constraints for language models in Syncfusion code studio IDE.
platform: syncfusion-code-studio
control: IDE
documentation: Getting Started
keywords: code, IDE, installation, windows, setup, getting-started
---

# Rules
 
**Rules** in Code Studio allow you to provide specific instructions that guide how the AI assistant behaves when working with your code. Instead of the AI making assumptions about your coding standards, architecture patterns, or project-specific requirements, you can explicitly define guidelines that ensure consistent, contextually appropriate responses.
 

## Purpose

- **Set Standards:** Ensure the AI follows your coding styles, guidelines, and project needs.
- **Keep Responses Consistent:** Ensure all answers align with your team’s requirements every time.
- **Easily Update Guidance:** Modify rules as your project evolves to maintain relevant suggestions.
- **Support Team Alignment:** Help everyone on the project receive guidance that matches shared practices.

## How Rules Work in Syncfusion Code Studio

 To form the system message, rules are joined with new lines, in the order they appear in the toolbar.

## How to Use Rules
 
### 1. Open Code Studio Extension
 
Click the **Syncfusion Code Studio** icon on the left toolbar to open the Syncfusion Code Studio chat window.
<img src="../reference-images/rule1.png" alt="rule" >

### 2. Add Rules 

Rules can be added locally using the “Add Rules” button. Navigate to the rules section and click the **Add Rules** button. This will open the config.yaml file.

<img src="../reference-images/rule2.png" alt="rule" >

In the `config.yaml` file, add a `rules` section.  Under this section, specify the rules or instructions you want the AI to follow. The AI will provide responses based on these defined rules.

#### Alternative: Create Your First Rule File

This is an alternative way to create Code Studio rules. You can use either the `config.yaml` rules section or this `.sfcoderules` file approach.

To set up a new rules file:
- Create a file called **.sfcoderules** at the top level of your workspace.Simply add your rules to this file, one per line. Save the file, and the AI will automatically use these rules to guide its responses.

<img src="../reference-images/rulesfile.png" alt="rule" >
 
### 3. Verify the Response
 
After adding the rules, give a query to the model. The response will be based on the rules you provided.

<img src="../reference-images/rule4.png" alt="rule" >
 
### 4. Edit the Rules

To edit rules, navigate to the rules section and click the pencil icon. This will open the `config.yaml` file, where you can modify the rules.

<img src="../reference-images/rule5.png" alt="rule" >