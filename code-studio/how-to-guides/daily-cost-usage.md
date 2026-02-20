---
title: "Track Daily Cost and Token Usage"
description: "How to view and filter daily costs and token usage in Syncfusion Code Studio"
classification: "User Guide - How To Documentation"
platform: syncfusion-code-studio
keywords: cost-usage, daily-cost, token-usage, budget, dashboard, analytics
---

# Track Daily Credits and Token Usage

## Overview
Daily credit and token tracking help you understand how much AI usage you are consuming.
It shows you:
- Total tokens used today
- Credits spent for today’s usage
- Usage patterns and unusual spikes
- Ways to optimize and reduce credit usage

This helps you manage your AI usage and stay within your available credits.

## When to Use
Use this tracking process when:
- You need to monitor credits usage on a daily basis.
- You're deploying LLM-based applications that may generate unpredictable or dynamic usage.
- You want to optimize prompt efficiency or identify expensive operations.

## Prerequisites
Ensure the following prerequisites are met before tracking credits and token usage in Code Studio:
- Syncfusion Code Studio is installed (see the [installation guide](/code-studio/getting-started/install-and-configuration)).
- You are signed in to Code Studio.
- You can access the Dashboard from within Code Studio Settings Account tab.
- The Usage Credits, and Tokens sections are visible on the dashboard.

## Steps to Check Daily Credits and Token Usage
Follow these steps to view your credits and token usage in Code Studio:

### Step 1: Open Code Studio
- Open Code Studio Application.
- Ensure you are logged in with the correct user credentials.

### Step 2: Open Account Settings
- In the top-right corner of Code Studio, click your **avatar**.
    
<img src="../how-to-guides/howtoguide-images/Avator-icon1.png">

- This opens the Account tab within the Settings page.  

### Step 3: Navigate to the Dashboard
- In the Account section, click **Open Dashboard**.
<img src="../how-to-guides/howtoguide-images/Dashboard-navigate1.png">
- You are redirected to the web dashboard where credits and usage information is displayed.

### Step 4: Select a Dashboard View
- In the dashboard, choose either the `Premium Model` or `Bring Your Own Key` tab.

    <img src="../how-to-guides/howtoguide-images/Dashboard-View.png">

### Step 5: Select Today’s Date
- In the dashboard, locate the date filter at the top of the page.
- Click the date field and select **Today**.
<img src="../how-to-guides/howtoguide-images/Date-filter1.png">

### Step 6: Select your name in the User field.
<img src="../how-to-guides/howtoguide-images/user-profile.png">
- The dashboard refreshes to show today’s credit usage.

### Step 7: View Daily Credit Usage
- After setting the date to **Today**, you see the total credit incurred today.
- This section represents your daily credit usage.
<img src="../how-to-guides/howtoguide-images/cost-usage.png">

### Step 8: Scroll down to view Token Usage
- Scroll down the dashboard page.
- Below the credits summary, you will find the Token Usage section.
<img src="../how-to-guides/howtoguide-images/Token-consumed.png">
Here is what you can track:
    - Token usage across different models you used today (hover over a model name).
    - Input vs. output token breakdown.
    - Total tokens consumed.
    - Model-specific token consumption trends.

> **Note:** To Check **BYOK** models credits and token usage, select the BYOK option at the top of the dashboard and repeat steps 5–8.
