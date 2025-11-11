---
title: Managing Users and Teams in Syncfusion Code Studio
description: Learn how to manage users, roles, and teams in Syncfusion Code Studio Enterprise Server for secure collaboration, governance, and usage visibility.
platform: syncfusion-code-studio
keywords: users, teams, roles, admin, team lead, invitations, access control, governance, syncfusion, code-studio, enterprise
---

# User & Teams

Code Studio empowers administrators and team leads to manage organization members, assign roles, and organize users into teams for seamless collaboration and governance.


## When to Use

- Admins & Team Leads: Invite users, assign roles, create teams, or reorganize members.
- Onboard new team members with correct role and team access.
- Update user roles (promote/demote) or team ownership.
- Clean up: rename, delete teams, or remove users.


## Prerequisites

- Administrator or Team Lead role.
- Valid email addresses for new users.
- Active Code Studio organization.
- Browser with internet access.




## 1. Teams Management

### Team List Panel

- Located on the left side of the interface.
- Displays all existing teams, such as:
  - BoldAgent Backend Team
  - BoldAgent Frontend Team
  - BoldBI-AI

### Selecting a Team

- Click on a team name to view its details.
- The selected team (e.g., BoldBI-AI-CodeStudio) will display its members and management options.

### Team Actions

Accessible via the context menu (three-dot icon):

- **Add Team**: Add a new team.
- **Rename Team**: Update the team name.
- **Add Team Member**: Invite new users to the team.
- **Set Team Owner**: Assign ownership for accountability.
- **Delete Team**: Remove the team from the organization.

<img src="./enterprise-images/addteamsenterprise.png" alt="user&Teams"  />

## 2. User Management

### Viewing Members

- The right panel shows team members.
- Each member can be managed individually.

### Adding Members

1. Click **“Invite User”** from the context menu.
2. Select the team from the dropdown.
3. Choose the role (Admin, Team Lead, User).
4. Enter the user’s email address.
5. Send the invitation. The user will be added upon acceptance.

<img src="./enterprise-images/invite user.png" alt="user&Teams"  />

### Editing or Removing Members

- Use the team panel to:
- **Edit** user's name or user's role.
- **Remove** users from the team.

<img src="./enterprise-images/edituserenterprise.png" alt="user&Teams"  />


## Validation

- **Invite Sent**: Email received with Accept Invite link.
- **User Added**: Appears in correct Team and Role column.
- **Role Change**: User sees new permissions (e.g., Budget tab appears for Team Lead).
- **Team Created**: Shows in left panel and can be selected.
- **Delete Team**: Team gone; members moved to Unassigned or removed.
- **Search**: Only matching users show in grid.


## Troubleshooting

- **“Invite User” button missing**  
  → You’re not Admin/Team Lead  
  → **Fix**: Ask Admin to promote you

- **User stuck in “Pending”**  
  → Invite not received or expired (24 hrs)  
  → **Fix**: Resend invite; check spam folder

- **Can’t change role**  
  → You’re Team Lead but not org Admin (can’t promote to Admin)  
  → **Fix**: Only Admins can assign Admin role

- **Team name won’t save**  
  → Name too long (>50 chars) or contains invalid symbols  
  → **Fix**: Use letters, numbers, spaces, hyphens

- **Deleted team still shows**  
  → Browser cache  
  → **Fix**: Hard refresh `Ctrl + Shift + R`

- **User in wrong team after move**  
  → Moved but old team still cached  
  → **Fix**: Refresh page; user should appear only in new team

- **No teams in left panel**  
  → First-time setup or all deleted  
  → **Fix**: Click **+ Add Team** to create one

