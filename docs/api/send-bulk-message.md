---
title: Send Bulk Message
sidebar_label: Messages
---

## Send Bulk Messages

Send messages to multiple recipients in a single API call.

---

### Parameters

| Name               | Type    | Required      | Description                                                                                                           |
|--------------------|---------|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `number`           | string  | Yes           | Recipient phone number in any format (digits only extracted internally).                                              |
| `message`          | string  | Conditionally | Text content of the message. Required for `text`, `buttons`, `interactive`, and optional for others.                  |
| `message_type`     | string  | Yes           | Type of message to send. One of: `text`, `image`, `video`, `audio`, `document`, `location`, `buttons`, `interactive`. |
| `media_url`        | string  | No            | URL of media file (image/video/audio/document) to send, depending on `message_type`.                                  |
| `file_name`        | string  | No            | File name for documents (e.g. `document.pdf`).                                                                        |
| `mimetype`         | string  | No            | MIME type of media, e.g., `image/jpeg`, `video/mp4`, `audio/mp4`, `application/pdf`.                                  |
| `latitude`         | number  | Required for `location` | Latitude coordinate for location messages.                                                                  |
| `longitude`        | number  | Required for `location` | Longitude coordinate for location messages.                                                                 |
| `buttons`          | array   | Required for `buttons`, `interactive` | Array of button objects for interactive messages. Each button should have `buttonId` and `displayText`.                                                                                                                                                         |
| `quoted_message_id`| string  | No            | ID of the message to quote (reply to).                                                                                |
| `quoted_message`   | string  | No            | Fallback text content for the quoted message if the original message is not found in the store.                       |

### API Endpoint

```http
POST https://app.rapiwa.com/api/send-bulk-message
```

### Header

```http
Content-Type: application/json
Authorization: Bearer Your_Device_Key
```

### Body

```http
{
  "numbers": ["+88017XXXXXXXX","+88017XXXXXXXX" ],
  "message_type": "image",
  "message": "Hello! Here is an image for you.",
  "media_url": "https://rapiwa.com/xyz.jpg",
  "mimetype": "image/jpeg"
}
```

###**Response:**


```bash
{
  "success": true,
  "results": [
      {
          "to": "88017XXXXXXXX",
          "message_id": "XXXXXXXXXXXXXXXXX",
          "success": true
      },
      {
          "to": "88017XXXXXXXX",
          "message_id": "XXXXXXXXXXXXXXXXX",
          "success": true
      }
  ]
}
```


> 💡 **Tip:** Keep your Device Key secure. Never share it publicly.
