---
title: Send Text Message
sidebar_label: Messages
---

## Send Basic Text Messages

Use this endpoint to send basic text messages. You can specify a single recipient phone number.

---

### Parameters

| Name               | Type    | Required      | Description                                                                                                           |
|--------------------|---------|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `number`           | string  | Yes           | Recipient phone number in any format (digits only extracted internally).                                              |
| `message`          | string  | Yes           | Text content of the message. Required for `text`, `buttons`, `interactive`, and optional for others.                  |
| `message_type`     | string  | Yes           | Type of message to send. One of: `text`, `image`, `video`, `audio`, `document`, `location`, `buttons`, `interactive`. |
| `media_url`        | string  | No            | URL of media file (image/video/audio/document) to send, depending on `message_type`.                                  |
| `file_name`        | string  | No            | File name for documents (e.g. `document.pdf`).                                                                        |
| `mimetype`         | string  | No            | MIME type of media, e.g., `image/jpeg`, `video/mp4`, `audio/mp4`, `application/pdf`.                                  |
| `latitude`         | number  | No            | Latitude coordinate for location messages.                                                                            |
| `longitude`        | number  | No            | Longitude coordinate for location messages.                                                                           |
| `buttons`          | array   | No            | Array of button objects for interactive messages. Each button should have `buttonId` and `displayText`.               |
| `quoted_message_id`| string  | No            | ID of the message to quote (reply to).                                                                                |
| `quoted_message`   | string  | No            | Fallback text content for the quoted message if the original message is not found in the store.                       |


### API Endpoint

```http
POST https://www.rapiwa.com/session/{API_Key}/send-message
```

### Body

```http
{
  "number": "88017XXXXXXXX",
  "message_type": "text",
  "message": "Hello!"
}
```

###**Response:**


```bash
{
    "success": true,
    "message_type": "text",
    "message_id": "3EB0FAC204D805F0E22293",
    "to": "8801759594891@s.whatsapp.net"
}
```


> 💡 **Tip:** Keep your API Key secure. Never share it publicly.
