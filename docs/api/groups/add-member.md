---
title: Add Member To Group
sidebar_label: Add Member
---

# Add Member to Group

This endpoint allows you to add one or more participants to an existing WhatsApp group.
You must supply a valid group_id and a list of phone numbers.

---

### Parameters

| Name               | Type    | Required      | Description                                                                                                           |
|--------------------|---------|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `group_id`         | string  | Yes           | The WhatsApp group JID (example: 12345@g.us).                                                                         |
| `participants`     | array   | Yes           | Array of phone numbers to be added to the group.                                                                      |


### API Endpoint

```http
POST https://app.rapiwa.com/api/group/add-member
```

### Header

```http
Content-Type: application/json
Authorization: Bearer Your_Device_Key
```

### Body

```http
{
  "group_id": "123XXXXXXXXXXXXXX@g.us",
  "participants": [
    "+88018XXXXXXXXX"
  ]
}
```

###**Response:**


```bash
{
    "success": true,
    "message": "Member added successfully",
    "data": {
        "status": true,
        "message": "Members added successfully",
        "result": [
            {
                "status": "200",
                "jid": "XXXXXXXXXXXXXXX@lid",
                "content": {
                    "tag": "participant",
                    "attrs": {
                        "jid": "XXXXXXXXXXXXXXX@lid",
                        "phone_number": "XXXXXXXXXXXXX@s.whatsapp.net"
                    }
                }
            }
        ]
    }
}
```


> 💡 **Tip:** Keep your Device Key secure. Never share it publicly.