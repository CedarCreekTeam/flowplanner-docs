---
publish: true
permalink: Getting-Started/Setting-Up-Your-First-Board
aliases:
  - Board setup
  - First board
---

# Setting up your first board

Your board is the public page where users submit feedback and vote on ideas. This guide walks you through the key settings to configure before you share your board URL.

> [!quote] A well-configured board is a well-trusted board
> Users who land on your board and see clear categories, a clean design, and real posts already there are far more likely to ==contribute their own ideas==.

## What your board includes

Every FlowPlanner board has three sections your visitors can access:

- **Feedback** -- the main list of submitted posts, sorted by votes
- **Roadmap** -- posts grouped by status (Planned, In Progress, Released)
- A **submit form** so visitors can add their own feedback

---

## Configure your board

### 1. Board name and description

Go to **Admin → Settings**. Set:

- **Board name** -- shown as the title in the header (e.g., "TickUp Feedback")
- **Description** -- a short sentence telling visitors what this board is for

> [!tip] Good board description examples
> - "Share ideas, vote on what you want, and follow our roadmap."
> - "Tell us what to build next. Your votes help us prioritize."

### 2. Set up categories

Categories let users tag their feedback and let your team filter it. Without categories, everything lands in one pile.

- Go to **Admin → Categories**
- Add 3--5 categories. Good starting points:
  - Feature Request
  - Bug
  - Improvement
  - Question

[[Categories|Learn more about categories →]]

### 3. Sign-in requirements

Decide whether users need an account to participate:

| Setting | Effect |
|---------|--------|
| **Anyone can submit** | Maximum submissions, lowest friction |
| **Sign in to submit** | Reduces spam, requires users to create an account |
| **Sign in to vote** | Balances openness with vote integrity |

Go to **Admin → Settings** to configure this.

### 4. Board visibility

- **Public** -- anyone with the URL can view your board (default)
- **Private** -- only invited members can view it

Most teams keep boards public. Private boards are useful during early alpha phases.

---

## Share your board

Once configured, share your board at:

```
https://yoursubdomain.flowplanner.io
```

> [!success] Where to share your board URL
> - In-app: a "Give feedback" link in your navigation or footer
> - Your product docs or changelog
> - Email signature or newsletters
> - Your README or GitHub repo (for developer tools)

---

**Next:** [[Categories]]
