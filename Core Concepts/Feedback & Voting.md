---
publish: true
permalink: Core-Concepts/Feedback-And-Voting
aliases:
  - Feedback
  - Voting
  - Posts
---

# Feedback & voting

Feedback posts are the core unit of FlowPlanner. Users submit them. Other users vote on them. Your team acts on them. The vote count is ==your most reliable signal== for what to build next.

> [!quote] Votes are prioritization data
> Every vote is a user saying "I want this too." When 47 people want the same thing, you know it's real.

## What a post contains

Every feedback post has:

- **Title** -- a short summary of the request
- **Description** -- optional detail explaining the need or use case
- **Category** -- the type of feedback (e.g., Feature Request, Bug)
- **Status** -- where it is in your workflow
- **Vote count** -- how many users have endorsed it
- **Comments** -- discussion between users and your team

---

## How voting works

Any visitor can vote on a post (depending on your [[Board Settings|sign-in settings]]).

- Each user gets **one vote per post**
- Votes cannot be changed to a different post -- only removed
- Posts are sorted by vote count by default
- The vote count is ==always visible== and drives the natural ranking of ideas

> [!note] Vote counts matter more over time
> In the first week your board is live, everything looks tied at 0--5 votes. Give it a month of real users. The signal becomes clear.

---

## The lifecycle of a post

```
Submitted → Reviewed → Categorized → Status set → Roadmap → Released
```

1. **User submits** a post with a title, description, and category
2. **Admin reviews** it in the admin panel -- may edit the title for clarity
3. **Status is set** to something meaningful (see [[Statuses]])
4. If it's being worked on, it moves to **Planned** or **In Progress** -- it now appears on the roadmap
5. When shipped, it's marked **Released** -- users who voted get notified

---

## Duplicate posts

Users often submit the same idea multiple times. This is normal.

- Encourage users to **search before submitting** (the submit form shows matching posts)
- When you receive a duplicate, close it and leave a comment pointing to the original
- Votes stay on their original post -- they don't merge automatically

---

## Post discovery

Users can find existing posts by:

- Browsing the full list sorted by votes
- Filtering by **category** or **status**
- Using the **search bar** to find posts by keyword

[[Filtering & Searching|Learn about filtering and search →]]

---

**Next:** [[The Roadmap]]
