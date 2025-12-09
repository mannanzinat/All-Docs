---
title: Leave Group
sidebar_label: Leave Group
---

# Leave Group

This endpoint allows the connected WhatsApp account to leave a specific group. The account must be a member of the group to successfully leave it.

---

### Parameters

| Name               | Type    | Required      | Description                                                                                                           |
|--------------------|---------|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `group_id`         | string  | Yes           | The WhatsApp group JID (example: 12345@g.us).                                                                         |


### API Endpoint

```http
POST https://app.rapiwa.com/api/group/leave
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
    "message": "Left group successfully",
    "data": {
        "status": true,
        "message": "Left group XXXXXXXXXXXXXXXX@g.us successfully"
    }
}
```


> 💡 **Tip:** Keep your Device Key secure. Never share it publicly.