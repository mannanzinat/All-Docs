---
title: Create Group
sidebar_label: Create Group
---

# Create Group

Creates a new WhatsApp group with a given name and a list of participants.

---

### Parameters

| Name               | Type    | Required      | Description                                                                                                           |
|--------------------|---------|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `group_name`       | string  | Yes           | The name of the new WhatsApp group.                                                                                   |
| `participants`     | array   | Yes           | A list of participant phone numbers.                                                                                  |


### API Endpoint

```http
POST https://app.rapiwa.com/api/group/create
```

### Header

```http
Content-Type: application/json
Authorization: Bearer Your_Device_Key
```

### Body

```http
{
  "group_name": "Your Group Name",
  "participants": [
    "+88017XXXXXXXX",
    "+88015XXXXXXXX"
  ]
}
```

###**Response:**


```bash
{
    "success": true,
    "data": {
        "status": true,
        "group_id": "123456789XXXXXXXXX@g.us",
        "subject": "BoooooM",
        "participants": [
            {
                "id": "123XXXXXXXXXXX@lid",
                "phoneNumber": "88013XXXXXXXX@s.whatsapp.net",
                "admin": "superadmin"
            },
            {
                "id": "201XXXXXXXXXXX@lid",
                "phoneNumber": "88017XXXXXXXX@s.whatsapp.net",
                "admin": null
            },
            {
                "id": "194XXXXXXXXXXX@lid",
                "phoneNumber": "88015XXXXXXX@s.whatsapp.net",
                "admin": null
            }
        ]
    }
}
```


> 💡 **Tip:** Keep your Device Key secure. Never share it publicly.