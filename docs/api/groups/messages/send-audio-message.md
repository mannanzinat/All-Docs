---
title: Send Audio Message
sidebar_label: Messages
---

## Send Audio Messages
Sends a message with a audio attached via a URL.

Send a message that includes a audio. Provide the audio via a publicly accessible URL in the media_url parameter. 

You can optionally include caption text in the message parameter.

****
> 💡 **Note:** Supported audio formats: AAC, MP3, OGG, AMR.


---

### Parameters

| Name               | Type    | Required      | Description                                                                                                           |
|--------------------|---------|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `group_id`         | string  | Yes           | The WhatsApp group JID (example: 12345@g.us).                                            |
| `message`          | string  | No           | Text content of the message. Required for `text`, `buttons`, `interactive`, and optional for others.                  |
| `message_type`     | string  | Yes           | Type of message to send. One of: `text`, `image`, `video`, `audio`, `document`, `location`, `buttons`, `interactive`. |
| `media_url`        | string  | Yes            | URL of media file (image/video/audio/document) to send, depending on `message_type`.                                  |
| `file_name`        | string  | No            | File name for documents (e.g. `document.pdf`).                                                                        |
| `mimetype`         | string  | Yes            | MIME type of media, e.g., `image/jpeg`, `video/mp4`, `audio/mp4`, `application/pdf`.                                  |
| `latitude`         | number  | No            | Latitude coordinate for location messages.                                                                            |
| `longitude`        | number  | No            | Longitude coordinate for location messages.                                                                           |
| `buttons`          | array   | No            | Array of button objects for interactive messages. Each button should have `buttonId` and `displayText`.               |
| `quoted_message_id`| string  | No            | ID of the message to quote (reply to).                                                                                |
| `quoted_message`   | string  | No            | Fallback text content for the quoted message if the original message is not found in the store.                       |


### API Endpoint

```http
POST https://app.rapiwa.com/api/group/send-message
```

### Header

```http
Content-Type: application/json
Authorization: Bearer Your_Device_Key
```

### Body

```http
{
  "group_id": "XXXXXXXXXXXX",
  "message_type": "audio",
  "media_url": "https://rapiwa.com/xyz.mp3",
  "mimetype": "audio/mp4"
}
```

###**Response:**


```bash
{
  "success": true,
  "message_type": "image",
  "message_id": "XXXXXXXXXXXXXXXXXXXXXX",
  "to": "XXXXXXXXXXXXX"
}
```


> 💡 **Tip:** Keep your Device Key secure. Never share it publicly.
