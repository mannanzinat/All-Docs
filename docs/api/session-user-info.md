---
title: Sessions User Info
sidebar_label: Sessions
---

## Get Session User Info

Retrieve information about the user connected to a specific WhatsApp session in Rapiwa.  
This endpoint is useful to check the connection status, basic account details, and profile picture.

---

### API Endpoint

```http
GET https://app.rapiwa.com/api/info
```

### Header

```http
Authorization: Bearer Your_API_Key
```

###**Response:**


```bash
{
    "connected": true,
    "sessionId": "XXXXXXXXXXXXXXX",
    "id": "XXXXXXXXXXXXXXXXXXXX",
    "name": "Rapiwa",
    "phone": "88013XXXXXXXX",
    "profilePic": "https:XXXXXXXXXXXXXXXXXXXXXXX"
}
```


> 💡 **Tip:** Keep your API Key secure. Never share it publicly.
