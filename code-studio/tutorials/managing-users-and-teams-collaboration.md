---
title: Managing Users and Teams - Collaboration Guide
description: Learn how to create teams, invite users, and monitor usage in Syncfusion Code Studio Enterprise Server.
platform: syncfusion-code-studio
keywords: teams, users, collaboration, enterprise, dashboard, token usage, team management, invitations, admin, team lead
---

# Managing Users and Teams: Collaboration Guide

## Overview

Welcome! In this tutorial, you'll learn how to set up and manage your team in Code Studio Enterprise Server. Think of it as organizing your development team just like you would organize folders on your computer—everything in the right place!

By the end of this guide, you'll be able to:
- **Create teams** for different projects (like "frontend-team" or "mobile-team")
- **Invite teammates** to join your organization with just their email
- **Watch how your team uses AI** by checking token usage and activity
- **Manage members** easily—move people between teams, change roles, or remove access

This tutorial is perfect for team leads and admins who want to get their team collaboration up and running quickly.

## Prerequisites

- **Code Studio Enterprise account** - See [Getting Started](../enterprise-server/getting-started)
- **Admin or Team Lead role** - Required for managing teams and users

## Understanding Key Terms

**Organization:** Your company's workspace in Code Studio.

**Team:** A group of developers (e.g., "frontend-team", "backend-team").

**Roles:**
- **Admin** - Full control over organization
- **Team Lead** - Manages their own team
- **User** - Uses Code Studio

**Tokens:** Units that measure AI usage (like credits).

---

## Step 1: Create a Team

Creating a team helps you organize developers working on similar projects.

**Quick Steps:**
1. Open Code Studio, then click the **avatar icon** in the top-left corner
<img src="../how-to-guides/howtoguide-images/Avator-icon1.png">
2. Click **Open Dashboard** from the menu
<img src="../how-to-guides/howtoguide-images/Dashboard-navigate1.png">
3. In the sidebar, click **Users and Teams**, then click **Teams**
4. Click the **Add** button (located near the search box)
5. Enter your team name in the text field
6. Click **Add Team** to create the team

> **Tip:** Use lowercase with hyphens (e.g., "frontend-team", "backend-team")

**For detailed instructions with screenshots**, see [User & Teams - Team Management](../enterprise-server/userandteams)

---

## Step 2: Invite Users

Add team members by inviting new users or adding existing organization members.

**Two Methods:**

**Invite New Users:**
1. From the Dashboard, click **Teams** in the sidebar
2. Select your team from the list
3. Click the **Add Users** button
4. Click **Invite New Users** option
5. Enter the email address, select the role, and click **Send Invitation**

**Add Existing Users:**
1. From the Dashboard, click **Teams** in the sidebar
2. Select your team from the list
3. Click the **Add Users** button
4. Click **Add Existing Users** option
5. Select users from the organization members list and add them

**For complete step-by-step guide**, see [User & Teams Documentation](../enterprise-server/userandteams)

---

## Step 3: Monitor Token Usage

Track how your team uses AI resources through the Dashboard.

**View Team Usage:**
1. Click the **avatar icon** in the top-left corner of Code Studio
2. Click **Open Dashboard** from the menu
3. Locate and click the **filter option** at the top of the dashboard
4. Select **Team** from the filter dropdown
5. Choose your team name from the list to view usage
6. You can also check token usage for a specific session by selecting the respective chat session from the list
7. Review the displayed metrics: Tokens, Requests, Top Users, Top Models

**View Individual Usage:**
1. Click the **filter option** at the top of the dashboard
2. Select **User** from the filter dropdown
3. Choose the team member's name from the list
4. Review their personal statistics and usage data

**Key Metrics to Track:**
- Total tokens consumed
- Number of requests
- Top 5 users by usage
- Most used AI models
- Average latency

**For detailed dashboard guide**, see [Dashboard Documentation](../enterprise-server/dashboard)

---

## Step 4: Manage Team Members

Common team management tasks:

**Move User to Different Team:**
1. In the Dashboard, click **Users and Teams** in the sidebar
2. Click **Teams**
3. Find the user you want to move
4. Click the three-dot menu (⋮) next to their name
5. Select **Change Team** and choose the new team

**Remove User from Team:**
1. Select the team from the list
2. Find the user you want to remove
3. Click the three-dot menu (⋮) next to their name
4. Select **Remove Member** to remove them from the team

**Change User Role:**
1. In the Dashboard, click **Users and Teams** in the sidebar
2. Click **Users**
3. Find the user whose role you want to change
4. Click the three-dot menu (⋮) next to their name
5. Select **Edit**
6. Change the role from the dropdown and save

**Edit or Delete Users:**
- Click the three-dot menu (⋮) next to any user to edit their details or remove them from the organization

**For complete management guide**, see [User & Teams Documentation](../enterprise-server/userandteams)

---

## Collaboration Features

### Shared Credit Pool

**What is a Shared Credit Pool?**

Think of credits as tokens that you spend every time you use AI features in Code Studio. Instead of each team member having their own separate credits, your entire organization shares one big pool of credits—like a shared bank account that everyone can use.

**How It Works:**
- When anyone on your team uses AI features (like code suggestions, chat, etc.), it uses credits from the shared pool
- All team members on Basic, Pro, and Enterprise plans share the same credit balance
- You can see how much your team is using and how many credits are left

**Why This Matters:**
- **No individual limits:** Team members don't run out of credits individually
- **Easy management:** You buy credits once for the whole team
- **Fair usage:** Everyone has access to AI features without worrying about personal limits

**To View Your Shared Credits:**
1. Click the **avatar icon** (top-left corner)
2. Select **Settings** from the menu
3. Click the **Credits** section
4. You'll see:
   - Total credits available in your pool
5. To see which team is using the most credits, go back to the **Dashboard**
6. Use the filter to view usage by team

**To Add More Credits:**
1. In the **Credits** section of Settings
2. Click **Buy Credits** button
3. Choose the amount you want to purchase
4. Complete the payment
5. New credits are added to your shared pool immediately

See [Settings - Credits](../enterprise-server/settings) for more details

### Role-Based Access

| Role | Permissions |
|------|-------------|
| **Admin** | Full control, billing, all teams |
| **Team Lead** | Manage own team only |
| **User** | Use Code Studio, view own usage |

### Budget Controls
Set spending limits per team and get alerts in chat window when approaching thresholds.

See [Create Budget Documentation](../enterprise-server/createbudget)

### Additional Features
- **Invitation Management:** Resend or cancel invitations - [User Management](../enterprise-server/userandteams)
- **Fallback Policies:** [Automatic Model Switching](../enterprise-server/fallback)

---

## Common Scenarios

### New Developer Joining
1. Click **Users and Teams** in the sidebar
2. Click **Teams** and select the appropriate team
3. Click **Add Users** button
4. Select **Invite New Users**
5. Enter the email address, select the role
6. Click **Invite** to send the invitation

### Team Reorganization
1. Create new teams as needed (see Step 1 above)
2. Move members to new teams using the **Change Team** option from their three-dot menu
3. Once a team is empty, you can delete the old team

### Developer Leaving
1. In the Dashboard, click **Users and Teams**, then **Users**
2. Find the user in the list
3. Click the **three-dot menu (⋮)** next to their name
4. Select **Delete** to remove them from the organization

### Budget Running Low
1. Open the Dashboard and check for high token usage
2. Click the **avatar icon** and select **Settings**
3. Navigate to **Credits**
4. Click **Buy Credits**, select the amount, and complete payment

### Wrong Team Invitation
- **Before acceptance:** Cancel the invitation from the Users and Teams page and resend a new one
- **After acceptance:** Find the user, click their three-dot menu, and use **Change Team** to move them to the correct team

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| **User didn't receive invitation** | Check spam folder, verify email, use **Resend Invitation** |
| **Can't delete team** | Move all members out first, then delete |
| **Dashboard shows no data** | Check date range, refresh page, contact support if persistent |
| **Can't access features** | Verify role permissions, check subscription plan |


## What's Next?

**Related Guides:**
- [Budget Alerts](../how-to-guides/budget-alert) - Set spending notifications
- [Daily Cost Usage](../how-to-guides/daily-cost-usage) - Track spending patterns
- [BYOK Models](../how-to-guides/add-BYOK-model) - Configure your own AI keys
- [Dashboard Analytics](../enterprise-server/dashboard) - Advanced metrics
- [Enterprise Settings](../enterprise-server/settings) - Organization configuration
- [User & Teams Management](../enterprise-server/userandteams) - Complete reference

---

