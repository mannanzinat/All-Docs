---
title: On WhatsApp
sidebar_label: Sessions
---

## Check If A Number Is On WhatsApp
Verifies if a given JID (WhatsApp ID) is registered on WhatsApp.

---

### Parameters

| Name               | Type    | Required      | Description                                                                                                           |
|--------------------|---------|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `number`           | string  | Yes           | Add Phone Number.                                              |


### API Endpoint

```http
POST https://app.rapiwa.com/api/on-whatsapp
```

### Header

```http
Content-Type: application/json
Authorization: Bearer Your_API_Key
```

### Body

```http
{
  "number": "88017XXXXXXXXX",
}
```

###**Response:**


```bash
{
    "success": true,
    "data": {
        "phone": "+88017XXXXXXXX",
        "exists": true,
        "jid": "88017XXXXXXXXXXXXX",
        "message": "✅ Number is on WhatsApp"
    }
}
```


> 💡 **Tip:** Keep your API Key secure. Never share it publicly.
