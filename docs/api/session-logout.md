---
title: Session Logout
sidebar_label: Sessions
---

## Session Logout

Terminate an active WhatsApp session in Rapiwa.  
Once logged out, the session will be disconnected from WhatsApp, and you will need to scan a new QR code to reconnect.

---

### API Endpoint

```http
POST https://app.rapiwa.com/api/logout
```

### Header

```http
Content-Type: application/json
Authorization: Bearer Your_Device_Key
```

###**Response:**


```bash
{
    "success": true
}
```


> 💡 **Tip:** Keep your Device Key secure. Never share it publicly.
