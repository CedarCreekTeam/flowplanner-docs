---
publish: true
permalink: API-Reference/Introduction
aliases:
  - API
  - API overview
  - Developer docs
---

# API introduction

The FlowPlanner API lets you integrate your feedback data with your own systems -- pull posts into your internal tools, push status updates from your deployment pipeline, or trigger webhooks when votes hit a threshold.

> [!quote] Your feedback data, your way
> The API gives you ==programmatic access to everything on your board== -- posts, votes, categories, statuses, and more.

## Base URL

All API requests are made to:

```
https://flowplanner.io/api
```

Subdomain-specific requests use:

```
https://yoursubdomain.flowplanner.io/api
```

---

## Authentication

All API requests require a bearer token. Generate your API key in **Admin → Settings → API**.

Include your key in the `Authorization` header:

```
Authorization: Bearer your_api_key_here
```

[[Authentication|Full authentication guide →]]

---

## Rate limits

The API enforces rate limits to ensure fair use. Current limits:

- **100 requests per minute** per API key
- **5,000 requests per day** per organization

If you exceed the limit, you'll receive a `429 Too Many Requests` response. Retry after the `Retry-After` header value (in seconds).

---

## Response format

All responses are JSON. Successful responses return a `2xx` status code. Errors return a structured error object:

```json
{
  "error": "NOT_FOUND",
  "message": "Post not found"
}
```

---

## Available endpoints

| Resource | Description |
|----------|-------------|
| `GET /feedback` | List all feedback posts |
| `GET /feedback/:id` | Get a single post |
| `PATCH /feedback/:id` | Update a post's status or category |
| `GET /categories` | List all categories |
| `POST /webhooks` | Register a webhook endpoint |

[[Authentication|Start with authentication →]] or jump to [[API Reference/Feedback|the feedback endpoints →]].

---

**Next:** [[Authentication]]
