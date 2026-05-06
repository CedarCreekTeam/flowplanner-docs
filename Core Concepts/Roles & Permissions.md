---
publish: true
permalink: Core-Concepts/Roles-And-Permissions
aliases:
  - Roles
  - Permissions
  - Access control
---

# Roles & permissions

FlowPlanner has two distinct groups of people: **your team** (who manage the board) and **your users** (who vote and submit feedback). Within your team, there are two roles with different levels of access.

> [!quote] Right access for the right people
> Not everyone on your team needs to change board settings. Roles let you ==give everyone what they need== without overexposing controls.

## Team roles

### Owner

The account that created the organization. The owner has full access to everything:

- All admin functions
- Billing and subscription management
- Deleting the organization
- Cannot be removed by other members

### Admin

Full access to all board management features:

- Review and triage feedback
- Set statuses and categories
- Reply to posts with comments
- Invite and remove other members
- Change board settings

> [!note] Admins cannot manage billing
> Only the organization owner can access subscription and billing settings.

### Member

Can view and triage feedback but has limited settings access:

- Review feedback in the admin panel
- Set statuses and categories
- Reply to posts
- Cannot invite or remove team members
- Cannot change board settings

---

## User roles (your board visitors)

Users who visit your public board are not "members" of your organization -- they're visitors. They can:

- Browse all public feedback
- Submit posts (if allowed by your sign-in settings)
- Vote on posts (if allowed)
- Leave comments (if allowed)

Visitors never have access to the admin panel.

---

## Permissions summary

| Action | Owner | Admin | Member | Visitor |
|--------|-------|-------|--------|---------|
| View admin panel | ✓ | ✓ | ✓ | -- |
| Triage and update posts | ✓ | ✓ | ✓ | -- |
| Comment on posts | ✓ | ✓ | ✓ | ✓ (if allowed) |
| Invite members | ✓ | ✓ | -- | -- |
| Change board settings | ✓ | ✓ | -- | -- |
| Manage billing | ✓ | -- | -- | -- |
| Delete organization | ✓ | -- | -- | -- |

---

**Next:** [[Your Public Board]]
