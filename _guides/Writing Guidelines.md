# Writing guidelines for FlowPlanner docs

Internal guide -- not published. Read this before writing or editing any article.

## Voice and tone

FlowPlanner docs are: **plain, precise, action-oriented**. No filler, no apologies, no enterprise-speak.

- "Click **Save**" -- not "The Save button should be clicked"
- "Go to Admin → Categories" -- not "Navigate to the categories section of the admin interface"
- Sentence case for all headings: "Setting up your board" -- not "Setting Up Your Board"

## Word list

**Always say:**
- FlowPlanner (capital F and P, one word)
- board (not "portal," "workspace," or "site")
- post or feedback (not "ticket," "issue," or "record")
- vote (not "upvote" or "like")
- category (not "tag" or "label")
- status (not "stage" or "state")
- admin (the role, lowercase)
- member (team member, lowercase)

**Never say:**
- CRM, platform, streamline, leverage, seamless, robust
- enterprise (except in the positioning line "without the enterprise tax")
- Cedar Creek in product copy

## Callout types

Use these consistently:

| Callout | Use for |
|---------|---------|
| `> [!quote]` | Opening tone-setter at the top of each article |
| `> [!tip]` | Helpful suggestions and best practices |
| `> [!success]` | Positive outcomes, what good looks like |
| `> [!note]` | Caveats, important limitations, things to be aware of |
| `> [!highlight]` | Key insights worth emphasizing inline |

## Highlights

Use `==highlighted text==` sparingly -- only for the most important phrase per section. Don't highlight whole sentences.

## Structure of every article

1. Frontmatter (`publish`, `permalink`, `aliases`)
2. H1 title (sentence case)
3. Opening `> [!quote]` callout
4. Body content
5. `---` separator
6. `**Next:** [[Link]]` to the logical next article

## Audience

Most docs are written for **admins** (people running their product's feedback board). The `Collecting Feedback/` section is written for **end users** (voters and submitters). Always be clear which audience you're addressing.

## Internal links

Use `[[Page Title]]` for all internal references. For custom display text: `[[Page Title|Click here]]`. Never use raw URLs for internal pages.

## When a feature ships

1. Read the relevant existing docs before editing
2. Check that feature names and UI terms exactly match what's in the app
3. Add a Release Notes entry
4. Update any articles that describe the old behavior
