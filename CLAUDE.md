# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with this repository.

## Project overview

FlowPlanner documentation site built with **Obsidian Publish**. The docs cover FlowPlanner -- a user feedback and public roadmap tool for product teams.

## Documentation framework

- **Platform:** Obsidian Publish (not Docusaurus/MkDocs)
- **Format:** Pure Markdown with Obsidian-specific syntax
- **Publishing:** Files with `publish: true` frontmatter are published

## Documentation conventions

### Frontmatter (required on every page)
```yaml
---
publish: true
permalink: Section-Name/Page-Title
aliases:
  - Alternative Name
---
```

### Formatting rules
- **Callouts:** Use `> [!quote]`, `> [!tip]`, `> [!success]`, `> [!note]`, `> [!highlight]` for emphasis blocks
- **Internal links:** Use `[[Page Title]]` wiki-link syntax, `[[Page|Custom Text]]` for custom display
- **Images:** Use `![[filename.png]]` for embedded images from `_assets/`
- **Bold** for UI elements and key terms, `code` for technical values and paths
- **Highlights:** `==highlighted text==` for key phrases worth calling out inline
- **Page endings:** Every page ends with `---` followed by `**Next:** [[Link]]`
- **Opening quotes:** Most pages start with a `> [!quote]` callout to set the tone

### Folder structure
- `Getting Started/` -- Onboarding and account setup
- `Core Concepts/` -- Boards, feedback, roadmap, statuses, categories, roles
- `Collecting Feedback/` -- End-user facing: submitting, voting, commenting
- `Managing Your Board/` -- Admin workflows: managing posts, categories, team, settings
- `Roadmap/` -- The public roadmap feature
- `Account & Settings/` -- Profile, billing, password
- `API Reference/` -- Developer docs
- `Pro Tips/` -- Power-user workflows
- `Release Notes/` -- Version history
- `_assets/` -- Images and media (excluded from publish)
- `_templates/` -- Obsidian templates (excluded from publish)
- `_guides/` -- Internal writing guides (excluded from publish)

### Writing style
- Professional but conversational tone
- Action-oriented with clear next steps
- Progressive disclosure (basics first, advanced later)
- Concrete examples with real-world scenarios
- Sentence case for all headings -- never title case

---

## Brand voice & writing standards

### What FlowPlanner is

FlowPlanner is a **user feedback and public roadmap tool** for product teams. It lets companies collect feedback from their users, let those users vote on ideas, and publish a public roadmap -- without enterprise pricing or complexity.

Positioning line: *"Collect feedback, let your users vote, ship a public roadmap -- without the enterprise tax."*

### Word list

**Always say:**
- **FlowPlanner** -- one word, capital F and P. Never "Flow Planner" or "flowplanner"
- **board** -- the public feedback portal for an org. Not "portal," "workspace," or "site"
- **post** or **feedback** -- what users submit. Not "ticket," "issue," or "request" (unless quoting a category name)
- **vote** -- not "upvote" or "like"
- **admin** -- the person managing the board. Not "owner" in copy (though it's the role name)
- **roadmap** -- lowercase unless referring to the UI tab/label
- **status** -- the workflow state of a post (Open, Planned, In Progress, Released, Closed)
- **category** -- grouping for posts. Not "tag," "label," or "type"
- **org** or **organization** -- the account that owns the board. Not "company" or "workspace" in UI copy
- **member** -- a team member with admin access. Not "user" or "admin user"

**Never say:**
- CRM (FlowPlanner is not a CRM)
- platform (say "FlowPlanner" or "your board")
- streamline, optimize, leverage, seamless, robust
- enterprise (unless in the positioning "without the enterprise tax")
- tickets, issues (unless that's how the user's category is named)
- Cedar Creek in product copy (footer and legal only)

### Tone for support docs

Plain, precise, zero ambiguity. Active voice. No filler.

- "Click **Save**" -- not "The Save button should be clicked"
- "Open the admin panel, go to **Feedback**, find the post" -- not "In order to successfully manage feedback..."
- No apologies for how the product works.

### Sentence case

All headings and callout titles use sentence case. Not title case.
- Right: "Setting up your board"
- Wrong: "Setting Up Your Board"

### Two audiences

Most docs are written for **admins** (the people running their product's feedback board). The `Collecting Feedback/` section is written for **end users** (the voters and feedback submitters).

Be clear about which audience you're addressing. "You" in admin docs = the admin. "Your users" = their voters/submitters.

### Pricing (confirm with app before publishing)

FlowPlanner uses a free + paid model. Check `internal/handlers/billing.go` and the Stripe config for current plan names and limits.

---

## FlowPlanner app reference

The app codebase lives at `/Users/lonnyhallsted/GitHub/flowplanner`. Key areas:
- **Backend:** Go + Iris framework (`internal/` directory)
- **Frontend:** Svelte 5 + Tailwind (`web/src/` directory)
- **Database:** PostgreSQL with migrations (`internal/database/migrations/`)
- **Models:** `internal/models/` (User, Organization, Feedback, Category, Comment, Vote)
- **Admin routes:** `/admin` prefix in the Go router
- **Public board:** Served at `<slug>.flowplanner.io`
