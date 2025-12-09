---
title: Get Group Metadata
sidebar_label: Group Metadata
---

# Get Group Metadata

Retrieves metadata for a specific WhatsApp group, such as subject, description, creation date, and owner.

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
    "message": "Group metadata fetched successfully",
    "data": {
        "status": true,
        "group_id": "12XXXXXXXXXXXXXX@g.us",
        "subject": "XXXXXX",
        "creation_time": XXXXXXXXX,
        "description": null,
        "owner": "XXXXXXXXXXXXXXX@lid",
        "subject_owner": "XXXXXXXXXXXXXXX@lid",
        "participants_count": 4,
        "participants": [
            {
                "id": "XXXXXXXXXXXXX@lid",
                "is_admin": false,
                "is_superadmin": false,
                "admin_type": "member"
            },
            {
                "id": "XXXXXXXXXXXXXX@lid",
                "is_admin": false,
                "is_superadmin": false,
                "admin_type": "member"
            }
        ],
        "raw": {
            "id": "XXXXXXXXXXXX@g.us",
            "addressingMode": "lid",
            "subject": "XXXXXXX",
            "subjectOwner": "XXXXXXXXXXXXX@lid",
            "subjectOwnerPn": "XXXXXXXXXXXXXX@s.whatsapp.net",
            "subjectTime": 1765257302,
            "size": 4,
            "creation": 1765257302,
            "owner": "XXXXXXXXXXXXX@lid",
            "ownerPn": "XXXXXXXXXXXXXX@s.whatsapp.net",
            "owner_country_code": "BD",
            "descTime": null,
            "restrict": false,
            "announce": false,
            "isCommunity": false,
            "isCommunityAnnounce": false,
            "joinApprovalMode": false,
            "memberAddMode": false,
            "participants": [
                {
                    "id": "XXXXXXXXXXXXX@lid",
                    "phoneNumber": "XXXXXXXXXXXXXX@s.whatsapp.net",
                    "admin": null
                },
                {
                    "id": "XXXXXXXXXXXXXX@lid",
                    "phoneNumber": "XXXXXXXXXXXXXXX@s.whatsapp.net",
                    "admin": null
                },
                {
                    "id": "XXXXXXXXXXXXX@lid",
                    "phoneNumber": "XXXXXXXXXXXXXX@s.whatsapp.net",
                    "admin": "superadmin"
                }
            ]
        }
    }
}
```


> 💡 **Tip:** Keep your Device Key secure. Never share it publicly.