---
title: Send Document Message
sidebar_label: Messages
---

## Send Document Messages
Sends a message with an document attached via a URL.

Send a message that includes an document. Provide the document via a publicly accessible URL in the media_url parameter. 

****
> 💡 **Note:** Most common document types are supported (PDF, DOCX, XLSX, etc.)


---

### Parameters

| Name               | Type    | Required      | Description                                                                                                           |
|--------------------|---------|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `number`           | string  | Yes           | Recipient phone number in any format (digits only extracted internally).                                              |
| `message`          | string  | No            | Text content of the message. Required for `text`, `buttons`, `interactive`, and optional for others.                  |
| `message_type`     | string  | Yes           | Type of message to send. One of: `text`, `image`, `video`, `audio`, `document`, `location`, `buttons`, `interactive`. |
| `media_url`        | string  | Yes            | URL of media file (image/video/audio/document) to send, depending on `message_type`.                                  |
| `file_name`        | string  | Yes            | File name for documents (e.g. `document.pdf`).                                                                        |
| `mimetype`         | string  | Yes            | MIME type of media, e.g., `image/jpeg`, `video/mp4`, `audio/mp4`, `application/pdf`.                                  |
| `latitude`         | number  | No            | Latitude coordinate for location messages.                                                                            |
| `longitude`        | number  | No            | Longitude coordinate for location messages.                                                                           |
| `buttons`          | array   | No            | Array of button objects for interactive messages. Each button should have `buttonId` and `displayText`.               |
| `quoted_message_id`| string  | No            | ID of the message to quote (reply to).                                                                                |
| `quoted_message`   | string  | No            | Fallback text content for the quoted message if the original message is not found in the store.                       |


### API Endpoint

```http
POST https://app.rapiwa.com/api/send-message
```

### Header

```http
Content-Type: application/json
Authorization: Bearer Your_Device_Key
```

### Body

```http
{
  "number": "88017XXXXXXXX",
  "message_type": "document",
  "media_url": "https://rapiwa.com/xyz.pdf",
  "file_name": "file.pdf",
  "mimetype": "application/pdf"
}
```

###**Response:**


```bash
{
  "success": true,
  "message_type": "document",
  "message_id": "XXXXXXXXXXXXXXXXXXX",
  "to": "88017XXXXXXXXX"
}
```


> 💡 **Tip:** Keep your Device Key secure. Never share it publicly.
