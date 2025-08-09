---
title: Sessions
sidebar_label: Sessions
---

## Get Your WhatsApp Session QR Code

Retrieve the QR code needed to link your WhatsApp device with Rapiwa.  
Use this endpoint to get the current QR code image or string to scan in your WhatsApp app.

---

### API Endpoint

```http
GET https://www.rapiwa.com/session/{API_Key}/qr
```

**Body:**

```bash
{
  "number": "88017XXXXXXXX",
  "message_type": "text",
  "message": "Hello from Postman!"
}
```

**Response:**

```bash
{
    "success": true,
    "message_type": "text",
    "message_id": "3EB0C9C1719F058FFABB63",
    "to": "88017XXXXXXXX@s.whatsapp.net"
}
```


> 💡 **Tip:** Keep your API Key secure. Never share it publicly.
