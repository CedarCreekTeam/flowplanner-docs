---
publish: true
permalink: Managing-Your-Board/Managing-Feedback
aliases:
  - Triage feedback
  - Review posts
---

# Managing feedback

The Feedback section of your admin panel is where you review incoming posts, set statuses, assign categories, respond to users, and keep your board organized.

> [!quote] Good feedback management is active listening at scale
> When users see their posts categorized and updated, they know ==someone is reading==. That trust keeps them coming back.

## The feedback list

Go to **Admin → Feedback**. You'll see all posts with columns for:

- **Title** -- the post name
- **Category** -- the type of feedback
- **Status** -- where it is in your workflow
- **Votes** -- how many users have endorsed it
- **Date** -- when it was submitted

---

## Filtering and sorting

Use the filter bar to narrow your view:

- Filter by **status** (Open, Planned, In Progress, Released, Closed)
- Filter by **category**
- Sort by votes, date, or recent activity

> [!tip] Start with Open, sorted by votes
> This is the highest-signal view -- the most-wanted unreviewed posts, ranked by user demand.

You can also filter the left-hand post list by status without changing your main view. Click the **funnel icon** next to the post count at the top of the nav panel to filter by any single status.

---

## Reviewing a post

Click any post to open it. From the detail view you can:

- **Edit the title** for clarity (useful when a submission is vague)
- **Set or change the status** -- see [[Statuses]]
- **Set or change the category**
- **Toggle roadmap visibility** -- pin a post to the roadmap without changing its status (see below)
- **Leave a comment** -- visible publicly to all board visitors
- **Delete the post** -- removes it from the board entirely

---

## Setting a status

The most important action you take on a post is setting its status. This tells your users where their feedback stands and drives what appears on the roadmap.

| You're doing | Set status to |
|-------------|--------------|
| Acknowledging but no decision yet | Open |
| Committed to building this | Planned |
| Actively working on it | In Progress |
| Shipped -- it's live | Released |
| Not building this | Closed |

[[Updating Statuses|More detail on status workflows →]]

---

## Adding a post to the roadmap

Any post can be pinned to the public roadmap directly from its detail view -- without changing its status. Look for the **Roadmap** section in the right sidebar and click **Add to roadmap**. The post will appear in the Planned column on your public roadmap.

This is useful when you want to highlight something publicly before you're ready to formally set a status like Planned or In Progress. Toggle it off at any time to remove it.

> [!note] Status-based roadmap still works the same
> Posts set to Planned, In Progress, or Released appear on the roadmap automatically. The manual toggle is just an extra way to feature a post.

---

## Bulk actions

Select multiple posts using the checkboxes in the post list. A bulk action bar appears at the bottom of the screen with options to:

- **Set status** -- apply a new status to all selected posts at once
- **Set category** -- assign a category to all selected posts
- **Add to roadmap / Remove from roadmap** -- toggle roadmap visibility for selected posts
- **Delete** -- permanently remove all selected posts

> [!warning] Bulk delete is permanent
> Deleted posts cannot be recovered. Use this to clean up spam or duplicates.

---

## Responding to posts

Leaving a comment on a post creates a public response that all users can see. Use comments to:

- Explain a decision ("We're planning this for next quarter")
- Ask for clarification ("Can you say more about your use case?")
- Close a post with context ("This is a duplicate of [link]. Please vote there instead.")

> [!success] Always comment when closing
> A post marked Closed with no explanation feels like being ignored. A post closed with ==a clear reason== feels like a decision. Always leave a note.

---

**Next:** [[Updating Statuses]]
