---
title: Join To Group
sidebar_label: Join To Group
---

# Join to Group

This endpoint allows a connected WhatsApp device to join a group using a valid WhatsApp invite link.
Once the join request succeeds, the API will return the group’s JID (xxx@g.us).

---

### Parameters

| Name               | Type    | Required      | Description                                                                                                           |
|--------------------|---------|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `invite_link`      | string  | Yes           | The WhatsApp group invite URL (e.g., https://chat.whatsapp.com/...)                                                   |
 

### API Endpoint

```http
POST https://app.rapiwa.com/api/group/join
```

### Header

```http
Content-Type: application/json
Authorization: Bearer Your_Device_Key
```

### Body

```http
{
  "invite_link": "https://chat.whatsapp.com/XXXXXXXXXXXXXXX"
}
```

###**Response:**


```bash
{
    "success": true,
    "message": "Joined group successfully",
    "data": {
        "status": true,
        "message": "Joined group successfully",
        "response": "XXXXXXXXXXXXXXX@g.us"
    }
}
```


> 💡 **Tip:** Keep your Device Key secure. Never share it publicly.