---
title: Delete Group
sidebar_label: Delete Group
---

# Delete Group

This endpoint enables the connected WhatsApp account to permanently delete a specific group. To successfully perform this action, the account must be a member of the group.

> **Note:** Only the group **super admin** has the permission to delete a group. Ensure that your account has the necessary privileges before making the request.

---

### Parameters

| Name               | Type    | Required      | Description                                                                                                           |
|--------------------|---------|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `group_id`         | string  | Yes           | The WhatsApp group JID (example: 12345@g.us).                                                                         |


### API Endpoint

```http
POST https://app.rapiwa.com/api/group/delete
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
    "message": "Delete group successfully",
    "data": {
        "status": true,
        "message": "Delete group XXXXXXXXXXXXXXXX@g.us successfully"
    }
}
```


> 💡 **Tip:** Keep your Device Key secure. Never share it publicly.