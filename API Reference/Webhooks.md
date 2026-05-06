---
publish: true
permalink: API-Reference/Webhooks
aliases:
  - Webhooks
  - Event notifications
---

# Webhooks

Webhooks let FlowPlanner push real-time notifications to your server when events happen on your board. Instead of polling the API, ==your system gets notified the moment something changes==.

> [!quote] React to feedback in real time
> When a post hits 50 votes or a status changes, your system can know ==immediately== -- no polling required.

## Registering a webhook

1. Go to **Admin → Settings → Webhooks**
2. Click **Add webhook**
3. Enter your **endpoint URL** -- a publicly accessible HTTPS endpoint on your server
4. Select the **events** you want to receive
5. Copy the **signing secret** -- you'll use this to verify incoming requests
6. Save

> [!note] HTTPS required
> Webhook endpoints must use HTTPS. HTTP endpoints are not accepted.

---

## Events

| Event | When it fires |
|-------|--------------|
| `feedback.created` | A new post is submitted |
| `feedback.status_changed` | A post's status is updated |
| `feedback.vote_added` | A user votes on a post |
| `comment.created` | A comment is posted on a feedback item |

---

## Webhook payload

Every webhook delivers a `POST` request to your endpoint with a JSON body:

```json
{
  "event": "feedback.status_changed",
  "timestamp": "2026-05-01T14:23:00Z",
  "data": {
    "post_id": "abc123",
    "title": "Add CSV export",
    "status": "released",
    "previous_status": "in_progress",
    "vote_count": 47
  }
}
```

---

## Verifying webhook signatures

Every request includes a `X-FlowPlanner-Signature` header containing an HMAC-SHA256 signature of the raw request body, signed with your webhook secret.

Verify the signature before processing any webhook:

```javascript
const crypto = require('crypto');

function verifyWebhook(body, signature, secret) {
  const expected = crypto
    .createHmac('sha256', secret)
    .update(body, 'utf8')
    .digest('hex');
  return `sha256=${expected}` === signature;
}
```

> [!note] Always verify signatures
> Skip signature verification only in local development. In production, ==reject any request that fails verification== to prevent spoofed events.

---

## Responding to webhooks

Your endpoint must respond with a `200 OK` within **5 seconds**. If it doesn't, FlowPlanner retries the delivery with exponential backoff (up to 3 attempts).

---

**Next:** [[Examples]]
