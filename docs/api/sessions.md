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
GET https://app.rapiwa.com/api/qr
```

### Header

```http
Authorization: Bearer Your_Device_Key
```

###**Response:**


```bash
{
  <html>
    <head><meta http-equiv="refresh" content="10" /></head>
    <body style="text-align: center; font-family: sans-serif;">
      <img style="margin:auto;" src="data:image/png;base64,....." />
    </body>
  </html>
}
```


> 💡 **Tip:** Keep your Device Key secure. Never share it publicly.
