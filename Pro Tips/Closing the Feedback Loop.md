---
publish: true
permalink: Pro-Tips/Closing-The-Feedback-Loop
aliases:
  - Feedback loop
  - Close the loop
---

# Closing the feedback loop

The single most powerful thing you can do with FlowPlanner is ==mark things Released when you ship them==. This sounds simple. Most teams don't do it consistently. The ones who do have dramatically more engaged users.

> [!quote] Closing the loop is the whole point
> Feedback without a response is a suggestion box. Feedback that turns into a Released post is ==proof that you listen==.

## What "closing the loop" means

When you mark a post Released, you're telling every user who voted on it: "We heard you. We built it. It's live." This is the moment the feedback cycle completes.

---

## Why most teams miss it

> [!note] The common failure modes
> 1. **"We'll do it later"** -- you ship the feature but forget to update the status
> 2. **"It's small"** -- the improvement isn't worth announcing, so the status never changes
> 3. **"We changed the scope"** -- the feature shipped differently than the original request, so it feels wrong to mark it Released

None of these are good enough reasons. ==Partial wins still deserve acknowledgment.==

---

## How to build the habit

> [!tip] Make status updates part of your release process
> Add "update FlowPlanner statuses" to your deployment checklist or sprint retrospective. It takes 5 minutes and pays dividends in user trust.

**A practical system:**
1. When you close a ticket in Linear/Jira, note the related FlowPlanner post ID
2. After deployment, batch-update all related posts to Released
3. Leave a brief comment: "Shipped in v2.4 -- [what specifically changed]"

---

## What to write when you mark something Released

A good Released comment:
- Confirms what shipped ("Added CSV export under Settings → Export")
- Notes any differences from the original request ("Currently exports all posts -- date filtering coming in a follow-up")
- Thanks the users who requested it (optional but appreciated)

> [!success] Example released comment
> "This shipped in today's update. You'll find the export button under Admin → Feedback → Export. Exports to CSV with all columns. Thanks to everyone who voted on this -- 62 people asked for it!"

---

## The compounding effect

Users who see their requests go Released don't churn. They:

- Submit more high-quality feedback (because it works)
- Refer others ("their team actually listens")
- Are more forgiving when things break (because they trust the process)

A board where things regularly move to Released ==creates a community==, not just a complaint box.

---

**Next:** [[Getting More Votes]]
