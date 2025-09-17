---
title: Create Budget in Syncfusion Code Studio
description: Learn how to configure team and individual user budgets, set budget periods with auto-renewal, and set up usage alerts in Syncfusion Code Studio Enterprise Server.
platform: syncfusion-code-studio
keywords: budget, usage, billing, alerts, teams, users, admin, syncfusion, code-studio, enterprise server, getting started
---

# Create Budget

The Budget feature in Code Studio enables administrators to allocate and monitor AI usage budgets for teams and individual users. This helps organizations manage costs effectively and optimize AI resource utilization.

> **Note**: Only admins and Team Leads can edit and assign budget for all.

<img src="./enterprise-images/budgetnew.png" alt="budget"  />


## 1. Team Budget Setup

**Steps:**

- Open the **Budget** window.
- Select the desired **Team**.
- Set the **Maximum Budget** for the team.
- Choose the **Budget Period**:
  - Monthly
  - Quarterly
  - Half-Yearly
  - Annually
- (Optional) Enable **Auto-Renewal** by checking the box. This will automatically reset the budget at the end of each period.

<img src="./enterprise-images/teambudget.png" alt="budget"  />

## 2. Individual User Budget Allocation

**Steps:**

- Within the selected team, give the user’s name to edit budget limit.
- For each user:
  - Set the **Maximum Budget**.
  - Define the **Budget Period**.
- Monitor usage and adjust as needed.

<img src="./enterprise-images/memberbudget.png" alt="budget"  />

## Usage Alerts

Administrators can set up alerts to notify when budget usage exceeds a defined threshold.

**Steps:**

- Open the **Edit usage Alert**.
- Set the **Usage Threshold** (e.g., 50%).
- Enter the **Email Subject Prefix** (required).
- Specify the **Recipients** for the alert (e.g., team leads or finance managers). An alert email will be sent to the recipient.
- Click **Update** to activate the alert.

<img src="./enterprise-images/alert.png" alt="budget"  />

🔔 Alerts help proactively manage budget overruns and ensure timely action.


