# Best Practice for Webhooks

* Your service (webhook-url) should send its HTTP response as fast as possible. If it waits too long the hook will fail and retry it.\

* Your endpoint should ALWAYS return a valid HTTP response.

```json
{
    "alert-id": 0 , // (a unique identifier of the ID),
    "alert-message-date": "2021-08-13T15:07:49.0482561Z",
    "rule-id": 0, // (the ID of the rule which was triggered),
    "rule-name": "Request Created Rule",
    "event-name": "connectivity.provisioning.request.created",
    "account": "",//String (your account id),
    "events": [
        {
            "id": 0, // (a unique ID of the event which was fired from KORE)",
            "data": {
                //The event data will go here
            }
        }
    ]
}
```
