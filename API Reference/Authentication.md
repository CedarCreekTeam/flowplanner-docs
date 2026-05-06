---
publish: true
permalink: API-Reference/Authentication
aliases:
  - API authentication
  - API key
  - Bearer token
---

# Authentication

All FlowPlanner API requests require a valid API key. Keys are scoped to your organization and carry the permissions of the role you assign them.

> [!quote] Keep your API key private
> Your API key provides full access to your organization's data. ==Never expose it in client-side code== or commit it to a public repository.

## Generating an API key

1. Go to **Admin → Settings → API**
2. Click **Generate key**
3. Copy the key immediately -- it won't be shown again in full

> [!note] Store your key securely
> Use an environment variable or a secrets manager. Never hardcode your API key in source code.

---

## Using your API key

Include your key as a Bearer token in the `Authorization` header of every request:

```http
GET /api/feedback
Host: flowplanner.io
Authorization: Bearer fp_live_your_key_here
```

---

## Key prefixes

FlowPlanner API keys use prefixes to indicate their type:

| Prefix | Type |
|--------|------|
| `fp_live_` | Production key -- acts on real data |
| `fp_test_` | Test key -- safe for development |

> [!tip] Use test keys during development
> Test keys behave the same as live keys but won't affect your real board data.

---

## Revoking a key

If a key is compromised:

1. Go to **Admin → Settings → API**
2. Click **Revoke** next to the key
3. The key is immediately invalidated
4. Generate a new key and update your integrations

---

## Error responses

| Status | Error code | Meaning |
|--------|-----------|---------|
| `401` | `UNAUTHORIZED` | No key provided or key is invalid |
| `403` | `FORBIDDEN` | Valid key but insufficient permissions |

---

**Next:** [[API Reference/Feedback|Feedback endpoints →]]
