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
POST https://www.rapiwa.com/session/{API_Key}/logout
```

###**Response:**


```bash
{
    "success": true
}
```


> 💡 **Tip:** Keep your API Key secure. Never share it publicly.
