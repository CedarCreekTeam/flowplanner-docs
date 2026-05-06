---
publish: true
permalink: API-Reference/Examples
aliases:
  - API examples
  - Code examples
---

# API examples

Common integration patterns using the FlowPlanner API.

> [!quote] Real integrations, real patterns
> These examples cover the most common ways teams ==connect FlowPlanner to the rest of their stack==.

---

## Auto-update status from a deployment pipeline

Mark posts Released automatically when you deploy a feature. Tag your deployment with post IDs and update them via the API.

```bash
# In your CI/CD pipeline (e.g., GitHub Actions)
curl -X PATCH https://yoursubdomain.flowplanner.io/api/feedback/abc123 \
  -H "Authorization: Bearer $FLOWPLANNER_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"status": "released"}'
```

> [!tip] How to link posts to deployments
> Store FlowPlanner post IDs in your PR description or commit message. Parse them in CI and update each one when the deployment succeeds.

---

## Sync top-voted posts to Linear or Jira

Pull your most-voted open posts and create issues in your project tracker:

```javascript
const posts = await fetch('https://yoursubdomain.flowplanner.io/api/feedback?status=open&sort=votes&limit=10', {
  headers: { Authorization: `Bearer ${process.env.FLOWPLANNER_KEY}` }
}).then(r => r.json());

for (const post of posts.data) {
  await createLinearIssue({
    title: post.title,
    description: `${post.vote_count} votes on FlowPlanner\n\n${post.description}`,
  });
}
```

---

## Notify Slack when a post hits 50 votes

Use a webhook to get notified when vote counts cross a threshold. Check the count in your webhook handler:

```javascript
app.post('/flowplanner-webhook', (req, res) => {
  const { event, data } = req.body;
  if (event === 'feedback.vote_added' && data.vote_count === 50) {
    sendSlackMessage(`🔥 "${data.title}" just hit 50 votes on FlowPlanner`);
  }
  res.status(200).send('ok');
});
```

---

## List all released posts for a changelog

Pull Released posts to power an automated changelog page or email digest:

```javascript
const released = await fetch('https://yoursubdomain.flowplanner.io/api/feedback?status=released&sort=newest', {
  headers: { Authorization: `Bearer ${process.env.FLOWPLANNER_KEY}` }
}).then(r => r.json());

// released.data is an array of posts sorted by most recently released
```

---

**Next:** [[Pro Tips/Closing the Feedback Loop|Closing the feedback loop →]]
