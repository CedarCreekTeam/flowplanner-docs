---
publish: true
permalink: Core-Concepts/Boards
aliases:
  - Board
  - Your board
---

# Boards

Your board is the ==public home for your product's feedback==. It's where users submit ideas, vote on what matters most, and browse your roadmap. It lives at a URL you own: `yourname.flowplanner.io`.

> [!quote] One URL for everything
> Your board is your product's public feedback page, your roadmap, and your "we're listening" signal -- all in one place.

## What a board contains

Every board has two public-facing sections:

**Feedback tab**
The main list of posts, sorted by votes by default. Users can filter by category, search for existing posts before submitting, and vote on ideas they care about.

**Roadmap tab**
Posts organized into status columns: Planned, In Progress, Released. Updated automatically as your team changes statuses.

---

## Your board URL

Your board is hosted at:
```
https://yoursubdomain.flowplanner.io
```

The subdomain is set during account creation and ==cannot be changed== without contacting support.

> [!tip] Where to link your board
> Add your board URL to your app's navigation, your email footer, your documentation, and anywhere users might want to give feedback. The more visible it is, the more signal you'll collect.

---

## What visitors can do

| Action | Requires sign-in? |
|--------|------------------|
| Browse feedback | No |
| Browse the roadmap | No |
| Submit a post | Configurable |
| Vote on a post | Configurable |
| Leave a comment | Configurable |

You control these sign-in requirements in [[Board Settings]].

---

## What your team can do

From the **admin panel** (accessible at `yourboard.flowplanner.io/admin`), your team can:

- Review all submitted feedback
- Set statuses and categories on posts
- Respond to posts with comments
- Invite other team members
- Configure board settings

[[Admin Overview|Open the admin panel guide →]]

---

## Board visibility

**Public boards** are visible to anyone with the URL -- no sign-in required to browse.

**Private boards** require users to have an account and be invited before they can view or participate.

Most teams run public boards. Private boards work well during early alpha or internal testing phases.

---

**Next:** [[Feedback & Voting]]
