---
title: Get Group Invite Link
sidebar_label: Get Group Invite Link
---

# Get Group Invite Link

Retrieves the invite link for a specific WhatsApp group. This link can be shared with others to allow them to join the group.

> **Note:** Only administrators of a group can generate an invite link. If the authenticated user is not an admin of the specified group, the request will fail.

---

### Parameters

| Name               | Type    | Required      | Description                                                                                                           |
|--------------------|---------|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `group_id`         | string  | Yes           | The WhatsApp group JID (example: 12345@g.us).                                                                         |


### API Endpoint

```http
POST https://app.rapiwa.com/api/group/invite-code
```

### Header

```http
Content-Type: application/json
Authorization: Bearer Your_Device_Key
```

### Body

```http
{
  "group_id": "12XXXXXXXXXXXXXXXX@g.us"
}
```

###**Response:**


```bash
{
    "success": true,
    "message": "Invite code retrieved successfully",
    "data": {
        "status": true,
        "group_id": "12XXXXXXXXXXXXX@g.us",
        "invite_code": "XXXXXXXXXXXXXXXX",
        "invite_link": "https://chat.whatsapp.com/XXXXXXXXXXXXXXXX"
    }
}
```


> 💡 **Tip:** Keep your Device Key secure. Never share it publicly.