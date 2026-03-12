---
title: "Fixing Collaboration Gaps: Managing Users and Teams in your organization using Code Studio's Enterprise Server"
description: "Learn how to create teams, invite users, and monitor usage in Syncfusion Code Studio Enterprise Server"
platform: syncfusion-code-studio
keywords: teams, users, collaboration, enterprise, dashboard, token-usage, team-management, invitations, admin, team-lead
---

# Fixing Collaboration Gaps: Managing Users and Teams in your organization using Code Studio's Enterprise Server


## Overview

This tutorial teaches you how to set up and manage your development team in Code Studio Enterprise Server. Whether you're organizing a small team or multiple departments, you'll learn everything needed to get your team collaborating effectively.

This tutorial is perfect for team leads and admins who want to get their team collaboration up and running quickly.

For more details on the features covered in this tutorial, see [User & Teams Management](/code-studio/enterprise-server/userandteams) and [Dashboard Analytics](/code-studio/enterprise-server/dashboard).

## Prerequisites

Before starting, ensure you have:

- Syncfusion Code Studio is installed and properly configured on your system. If you have not yet downloaded Code Studio, refer to [Install and Configure](/code-studio/getting-started/install-and-configuration) for step-by-step instructions.
- **Code Studio Enterprise account** — If not set up, see [Enterprise Server Getting Started Guide](/code-studio/enterprise-server/getting-started)
- **Admin or Team Lead role** — You'll need one of these roles to create teams and invite users

## What You Will Learn

By the end of this tutorial, you'll be able to:

- Create and organize teams for different projects
- Invite new developers and add existing members to teams
- Monitor AI usage across your organization with the Dashboard
- Manage team members (move between teams, change roles, remove access)
- Handle common scenarios like team reorganization and developer onboarding

## Key Concepts

Before we begin, let's define the important concepts:

| Term | Definition | Example |
|------|------------|---------|
| **Organization** | Your company's workspace in Code Studio | "Acme Corp Development" |
| **Team** | A group of developers working together | "frontend-team", "mobile-team" |
| **Admin** | Role with full control over the organization | Can manage all teams, billing, and settings |
| **Team Lead** | Role that manages a specific team | Can only manage their assigned team |
| **User** | Role for developers using Code Studio | Can code with AI features, view own usage |
| **Tokens** | Units measuring AI usage (like credits) | Each AI request consumes tokens |
| **Avatar Icon** | Your profile picture or initials in a circle | Located in top-left corner of Code Studio |
| **Dashboard** | Web-based admin interface for managing teams | Where you create teams, invite users, view analytics |


## Steps to Manage Teams and Users

### Step 1: Create a Team

### What Are Teams?

Teams are organizational units that group developers working together. They help you segment your organization by project, department, technology stack, or any structure that makes sense for your workflow.

### Why Use Teams?

- **Budget Control** — Allocate specific token budgets to different teams
- **Usage Tracking** — Monitor which teams consume the most AI resources
- **Access Management** — Easily assign or revoke access for entire groups
- **Collaboration** — Team members can see each other's usage patterns and share best practices

### Common Use Cases

- **By Project:** `web-app-team`, `mobile-app-team`, `api-services-team`
- **By Technology:** `frontend-team`, `backend-team`, `devops-team`
- **By Department:** `engineering-team`, `qa-team`, `data-science-team`
- **By Client:** `client-acme-team`, `client-globex-team` (for agencies)

### How to Create Teams

**To create teams with detailed step-by-step instructions and screenshots,** see [User & Teams - Team Management Documentation](/code-studio/enterprise-server/userandteams)


### Step 2: Invite Users

### What Is User Invitation?

Code Studio provides two ways to add members to your teams:
- **Invite New Users** — Send email invitations to people who don't have accounts yet
- **Add Existing Users** — Assign existing organization members to additional teams

### Why Use User Invitations?

- **Controlled Onboarding** — New hires receive structured access to the right teams from day one
- **Role Assignment** — Assign appropriate permissions (User, Team Lead, Admin) during invitation
- **Audit Trail** — Track who invited whom and when through the Dashboard
- **Flexible Management** — Move people between teams as projects evolve without creating new accounts

### Common Use Cases

**Invite New Users When:**
- Onboarding new employees who need Code Studio access
- Expanding your organization with new hires

**Add Existing Users When:**
- Someone switches projects and needs access to a different team
- A developer needs to work on multiple projects simultaneously (multi-team membership)
- Reorganizing teams without creating new accounts

### How to Invite Users

**To invite users with detailed step-by-step instructions and screenshots,** see [User & Teams Documentation](/code-studio/enterprise-server/userandteams)


### Step 3: Monitor Token Usage

### What Is Token Usage Monitoring?

The Dashboard provides real-time analytics showing how your organization consumes AI resources (measured in tokens). You can view usage at three levels:
- **Team-level** — Individual team statistics and trends
- **User-level** — Personal usage for specific developers

### Why Monitor Token Usage?

- **Cost Control** — Identify which teams or users consume the most resources before budgets are exceeded
- **Usage Patterns** — Discover peak usage times, preferred AI models, and workflow trends
- **Training Needs** — Spot developers who might benefit from AI best practices training
- **Capacity Planning** — Make informed decisions about credit purchases and budget allocations
- **Fair Distribution** — Ensure all teams have equitable access to AI resources

### Key Metrics Available

The Dashboard displays comprehensive usage data:

| Metric | What It Shows | How to Use It |
|--------|---------------|---------------|
| **Total Tokens Consumed** | Cumulative AI usage | Track spending against budget |
| **Number of Requests** | Query volume | Measure team activity levels |
| **Top 5 Users** | Highest consumers | Identify power users or anomalies |
| **Most Used AI Models** | Model preferences | Optimize model selection per team |
| **Session History** | Individual chat sessions | Review specific interactions |

### Common Use Cases

- **Weekly Reviews** — Check team dashboards every Monday to spot trends
- **Budget Alerts** — Monitor usage when approaching monthly limits
- **Onboarding Analysis** — Track new developer usage to gauge adoption
- **Performance Optimization** — Identify if certain models work better for specific teams
- **Audit Requirements** — Generate reports for compliance or billing purposes

### How to Access Usage Data

**To monitor token usage with detailed instructions on accessing all metrics and reports,** see [Dashboard Documentation](/code-studio/enterprise-server/dashboard)


### Step 4: Manage Team Members

### What Is Team Member Management?

As your organization evolves, you'll need to perform ongoing maintenance tasks like moving people between teams, updating permissions, or removing access. Code Studio provides flexible management options through the Dashboard.

### Why Manage Team Members?

- **Project Changes** — Developers switch projects frequently; team assignments should follow
- **Promotions** — Update roles when someone becomes a team lead or gains admin responsibilities
- **Departures** — Quickly revoke access when employees leave the organization
- **Reorganizations** — Restructure teams without losing historical data or creating new accounts
- **Security** — Maintain principle of least privilege by adjusting permissions as needed

### Common Management Tasks

The Dashboard supports these key operations:

| Task | When to Use It | Impact |
|------|----------------|--------|
| **Move User to Different Team** | Developer switches projects | User sees new team in Code Studio; access to old team removed |
| **Remove from Team** | Project ends, but user stays in organization | Removed from specific team; other team memberships unaffected |
| **Change User Role** | Promotions or permission adjustments | New role takes effect immediately; historical data preserved |
| **Delete User from Organization** | Employee termination | Complete removal; cannot be undone; must re-invite to restore |

### Important Considerations

**Role Changes:**
- **User → Team Lead** — Can now manage their assigned team
- **Team Lead → Admin** — Gains full organization control (use with caution!)
- **Admin → User** — Loses all administrative privileges immediately

**Deletion vs. Removal:**
- **Remove from Team** — User stays in organization, just leaves specific team
- **Delete User** — Permanent removal from entire organization; requires email confirmation

**Data Retention:**
- Historical usage data is preserved even after user deletion
- Budget and billing reports remain accurate for audit purposes

### How to Manage Members

**To perform member management tasks with detailed workflows and screenshots,** see [User & Teams Documentation](/code-studio/enterprise-server/userandteams)


## Verify Your Results

Let's make sure your team setup is complete! Follow these simple checks:

- **Check Your Teams** - Open the Dashboard  and verify you can see your created teams in the Users and Teams → Teams section with the correct members assigned.

- **Test User Access** - If you invited new users, confirm they received invitation emails and can log in. If you added existing users, verify they can see their new team in Code Studio.

- **Review Usage Metrics** - Navigate to the Dashboard and use the filter to view your team's token usage. Confirm the metrics are displaying correctly and you can drill down into individual user sessions.

- **Verify Permissions** - Check that team members have the correct roles (Admin, Team Lead, or User) by viewing the Users list in the Dashboard. Test that permissions work as expected.

**Congratulations!** 🎉 You've successfully set up team collaboration in Code Studio Enterprise Server. Your team can now work together with shared AI resources, clear role definitions, and centralized monitoring.



