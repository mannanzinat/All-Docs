---
title: Receive Message
sidebar_label: Webhooks
---

# Receive Messages

The **Receive Message** webhook is triggered whenever a new WhatsApp message is received in your session.  

This webhook delivers structured JSON data with:  

- **Session details** (session ID, message ID, timestamp)  
- **Sender information** (contact ID, name, JID)  
- **Message content** (text, media, interactive, etc.)  
- **Media metadata** (URL, file size, MIME type, location coordinates, button metadata)  

---

## Payload Structure

| Field          | Type     | Description |
|----------------|----------|-------------|
| `session_id`   | string   | Unique ID of the active WhatsApp session. |
| `from`         | string   | WhatsApp JID of the sender (e.g. `8801759594891@s.whatsapp.net`). |
| `contact_id`   | string   | Sender’s phone number (without WhatsApp suffix). |
| `name`         | string   | Sender’s saved contact name (if available). |
| `message_id`   | string   | Unique identifier for the message. |
| `message_type` | string   | Type of message (`text`, `image`, `video`, `document`, `audio`, `location`, `interactive`, `sticker`). |
| `message`      | string   | Message body (text or caption). |
| `timestamp`    | string   | UNIX timestamp of when the message was sent. |
| `media_info`   | object   | Media metadata (present for media/interactive messages). |

---

## Example Payloads

### 1. Text Message
```bash
{
  "session_id": "XXXXXXXXXXXXXXXXX",
  "from": "XXXXXXXXXXXXXXX",
  "contact_id": "88017XXXXXXXXXX",
  "name": "XXXXXXXXX",
  "message_id": "XXXXXXXXXXXXXXXXXXXXXXXXXX",
  "message_type": "text",
  "message": "Hello",
  "timestamp": "1755923552",
  "media_info": []
}
```

### 2. Image Message
```bash
{
  "session_id":"XXXXXXXXXXXXXXXXXXXX",
  "from":"XXXXXXXXXXXXX",
  "message":"XXXXXXXXXXX",
  "contact_id":"88017XXXXXXXX",
  "name":"XXXXXX",
  "message_id":"XXXXXXXXXXXXXXXXXXXXXXXXX",
  "message_type":"image",
  "timestamp":"1755925686",
  "media_info":
  {
    "mimetype":"image/jpeg",
    "fileName":"XXXXXXX",
    "file_url":"abc.jpeg"
  }
}
```

### 3. Video Message
```bash
{
  "session_id":"XXXXXXXXXXXXXXXXXXXX",
  "from":"XXXXXXXXXXXXX",
  "message":"XXXXXXXXXXX",
  "contact_id":"88017XXXXXXXX",
  "name":"XXXXXX",
  "message_id":"XXXXXXXXXXXXXXXXXXXXXXXXX",
  "message_type":"video",
  "timestamp":"1755925686",
  "media_info":
  {
    "mimetype":"video/mp4",
    "fileName":"",
    "file_url":"http://abc.mp4"
  }
}
```

### 4. Document Message
```bash
{
  "session_id":"XXXXXXXXXXXXXXXXXXXX",
  "from":"XXXXXXXXXXXXX",
  "message":"XXXXXXXXXXX",
  "contact_id":"88017XXXXXXXX",
  "name":"XXXXXX",
  "message_id":"XXXXXXXXXXXXXXXXXXXXXXXXX",
  "message_type":"document",
  "timestamp":"1755925686",
  "media_info":
  {
    "mimetype":"application/pdf",
    "fileName":"abc.pdf",
    "file_url":"http://abc.pdf"
  }
}
```

### 5. Audio Message
```bash
{
  "session_id":"XXXXXXXXXXXXXXXXXXXX",
  "from":"XXXXXXXXXXXXX",
  "message":"XXXXXXXXXXX",
  "contact_id":"88017XXXXXXXX",
  "name":"XXXXXX",
  "message_id":"XXXXXXXXXXXXXXXXXXXXXXXXX",
  "message_type":"audio",
  "timestamp":"1755925686",
  "media_info":
  {
    "mimetype":"audio/ogg; codecs=opus",
    "fileName":"abc.ogg",
    "file_url":"http://abc.ogg"
  }
}
```

### 6. Location Message
```bash
{
  "session_id":"XXXXXXXXXXXXXXXXXXXX",
  "from":"XXXXXXXXXXXXX",
  "message":"https://www.google.com/maps?q=23.8397235,90.3762095",
  "contact_id":"88017XXXXXXXX",
  "name":"XXXXXX",
  "message_id":"XXXXXXXXXXXXXXXXXXXXXXXXX",
  "message_type":"location",
  "timestamp":"1755925686",
  "media_info":
  {
    "latitude": 23.8397235,
    "longitude": 90.3762095,
  }
}
```


> 💡 **Tip:** Keep your Device Key secure. Never share it publicly.
