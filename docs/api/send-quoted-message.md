---
title: Send Quoted Message
sidebar_label: Messages
---

## Send Quoted Messages
Send a message that quotes or replies to a previous message. This is useful for maintaining conversational context.

To send a quoted message, include the quoted_message_id parameter with the ID of the message you want to reply to. The message ID (msgId) is returned in the success response of any message you send.

You can reply to any type of message (text, image, document, etc.) by providing quoted_message_id along with the content of your new message. If the original message is not found in the store, you can include the quoted_message parameter as a fallback text to display in the quoted bubble.


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
| `quoted_message_id`| string  | Yes            | ID of the message to quote (reply to).                                                                                |
| `quoted_message`   | string  | Yes            | Fallback text content for the quoted message if the original message is not found in the store.                       |


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
  "message_type": "text",
  "message": "This is my reply!",
  "quoted_message_id": "XXXXXXXXXXXXXXXXXXXXXXXXXXXX",
  "quoted_message": "Original message text here"
}
```

###**Response:**


```bash
{
  "success": true,
  "message_type": "text",
  "message_id": "XXXXXXXXXXXXXXXXXXXXX",
  "to": "88017XXXXXXXX"
}
```


> 💡 **Tip:** Keep your Device Key secure. Never share it publicly.
