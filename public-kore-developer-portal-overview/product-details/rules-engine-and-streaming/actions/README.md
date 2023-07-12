---
description: >-
  When creating a rule, the user can specify one or many actions for the rule.
  Each action has its own unique set of properties which are needed to trigger
  the action. To see all available actions, the
---

# Actions

```json
[
    {
        "type": "Webhook",
        "description": "An action which triggers a web notification whenever a KORE event is generated, use this action to listen for specific events; when an event is generated KORE will send a HTTP POST request with event data to the webhook URL.",
        "attributes": [
            {
                "name": "webhook-url",
                "description": "Valid URL to be use to send a HTTP post request",
                "type": "string"
            },
            {
                "name": "access-token",
                "description": "(Optional) specify a secret token, Kore will send POST request with “X-Kore-Notification” HTTP header, you can use this value to verify your request.",
                "type": "string"
            }
        ]
    }
]
```

The properties of the response are

* Type: Defines the action type which the user adds to a rule
* Description: A description of the action type
* Attributes: The properties required to set up the action for the rule
