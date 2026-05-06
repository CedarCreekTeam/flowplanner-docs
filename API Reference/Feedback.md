---
publish: true
permalink: API-Reference/Feedback
aliases:
  - Feedback API
  - Feedback endpoints
---

# Feedback endpoints

Use the feedback endpoints to retrieve posts, update their statuses and categories, or integrate FlowPlanner data into your internal tooling.

> [!quote] Connect FlowPlanner to your workflow
> Update post statuses from your ==deployment pipeline==, sync feedback to your internal tracker, or build a custom dashboard on top of your board data.

## List feedback posts

```http
GET /api/feedback
Authorization: Bearer your_api_key
```

**Query parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `status` | string | Filter by status: `open`, `planned`, `in_progress`, `released`, `closed` |
| `category_id` | string | Filter by category UUID |
| `sort` | string | Sort order: `votes` (default), `newest`, `trending` |
| `limit` | integer | Number of results (default: 25, max: 100) |
| `offset` | integer | Pagination offset |

**Response:**

```json
{
  "data": [
    {
      "id": "abc123",
      "title": "Add CSV export",
      "description": "We need a way to export all feedback to CSV...",
      "status": "planned",
      "category": { "id": "cat_1", "name": "Feature Request" },
      "vote_count": 47,
      "created_at": "2026-04-15T10:23:00Z"
    }
  ],
  "total": 142,
  "limit": 25,
  "offset": 0
}
```

---

## Get a single post

```http
GET /api/feedback/:id
Authorization: Bearer your_api_key
```

Returns the full post object including comments.

---

## Update a post

```http
PATCH /api/feedback/:id
Authorization: Bearer your_api_key
Content-Type: application/json
```

**Request body:**

```json
{
  "status": "released",
  "category_id": "cat_1"
}
```

Both fields are optional -- include only what you want to change.

> [!tip] Automate status updates from CI/CD
> Trigger a `PATCH` with `status: "released"` from your deployment pipeline whenever a feature ships. Your roadmap updates automatically.

---

## Feedback statuses

| API value | Board display |
|-----------|--------------|
| `open` | Open |
| `planned` | Planned |
| `in_progress` | In Progress |
| `released` | Released |
| `closed` | Closed |

---

**Next:** [[Webhooks]]
