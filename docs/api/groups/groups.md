---
title: Get All Groups
sidebar_label: Get All Groups
---

# Grops

Retrieve a list of all WhatsApp groups that the connected WhatsApp account is currently a part of. The response includes group ID, name, participants, creation time, and owner.

---

### API Endpoint

```http
GET https://app.rapiwa.com/api/groups
```

### Header

```http
Content-Type: application/json
Authorization: Bearer Your_Device_Key
```

###**Response:**


```bash
{
    "status": true,
    "total": 3,
    "groups": [
        {
            "group_id": "12XXXXXXXXXXXXX@g.us",
            "name": "12XXXXXXXXXXXXXX",
            "unreadCount": 1,
            "messageCount": 0
        },
        {
            "group_id": "12XXXXXXXXXXXXX@g.us",
            "name": "12XXXXXXXXXXXXXX",
            "unreadCount": 1,
            "messageCount": 0
        },
        {
            "group_id": "12XXXXXXXXXXXXX@g.us",
            "name": "12XXXXXXXXXXXXXX",
            "unreadCount": 1,
            "messageCount": 0
        }
    ]
}
```


> 💡 **Tip:** Keep your Device Key secure. Never share it publicly.