---
title: Send Locationo
sidebar_label: Messages
---

## Send Location
Sends a message containing a location pin.

Send a message containing a location pin. Provide the latitude and longitude within the location object parameter. You can optionally include a name and address for the location.

---

### Parameters

| Name               | Type    | Required      | Description                                                                                                           |
|--------------------|---------|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `number`           | string  | Yes           | Recipient phone number in any format (digits only extracted internally).                                              |
| `message`          | string  | No           | Text content of the message. Required for `text`, `buttons`, `interactive`, and optional for others.                  |
| `message_type`     | string  | Yes           | Type of message to send. One of: `text`, `image`, `video`, `audio`, `document`, `location`, `buttons`, `interactive`. |
| `media_url`        | string  | No            | URL of media file (image/video/audio/document) to send, depending on `message_type`.                                  |
| `file_name`        | string  | No            | File name for documents (e.g. `document.pdf`).                                                                        |
| `mimetype`         | string  | No            | MIME type of media, e.g., `image/jpeg`, `video/mp4`, `audio/mp4`, `application/pdf`.                                  |
| `latitude`         | number  | Yes            | Latitude coordinate for location messages.                                                                            |
| `longitude`        | number  | Yes            | Longitude coordinate for location messages.                                                                           |
| `buttons`          | array   | No            | Array of button objects for interactive messages. Each button should have `buttonId` and `displayText`.               |
| `quoted_message_id`| string  | No            | ID of the message to quote (reply to).                                                                                |
| `quoted_message`   | string  | No            | Fallback text content for the quoted message if the original message is not found in the store.                       |


### API Endpoint

```http
POST https://www.rapiwa.com/session/{API_Key}/send-message
```

### Header

```http
Content-Type: application/json
```

### Body

```http
{
  "number": "88017XXXXXXXXX",
  "message_type": "location",
  "latitude": 37.7749,
  "longitude": -122.4194
}
```

###**Response:**


```bash
{
  "success": true,
  "message_type": "location",
  "message_id": "XXXXXXXXXXXXXXXXXXXXX",
  "to": "88017XXXXXXXXXXX"
}
```


> 💡 **Tip:** Keep your API Key secure. Never share it publicly.
