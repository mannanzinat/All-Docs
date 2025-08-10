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
GET https://www.rapiwa.com/session/{API_Key}/info
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
