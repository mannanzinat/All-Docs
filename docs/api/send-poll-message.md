---
title: Send Poll Message
sidebar_label: Messages
---

## Send Poll Messages

This endpoint allows you to send different types of messages—including text, media, location, and polls—to a specific WhatsApp group by providing the group's JID.

---

### Parameters

| Name                     | Type      | Required | Description                                                                                         |
|--------------------------|-----------|----------|-----------------------------------------------------------------------------------------------------|
| `number`                 | string    | Yes           | Recipient phone number in any format (digits only extracted internally).                                  |
| `message_type`           | string    | Yes      | Type of message to send. Supported: `poll`.                                                         |
| `poll_name`              | string    | Yes       | Title of the poll (required when `message_type = poll`).                                            |
| `poll_options`           | array     | Yes       | List of poll options (required for poll messages).                                                  |
| `allow_multiple_answers` | boolean   | Yes       | Whether users can select more than one answer in the poll.                                          |

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
  "number": "+88017XXXXXXXXX",
  "message_type": "poll",
  "poll_name": "Best color?",
  "poll_options": ["Red", "Blue", "Green"],
  "allow_multiple_answers": false
}
```

###**Response:**


```bash
{
    "success": true,
    "message_type": "text",
    "message_id": "3EB0FAC204D805F0E22293",
    "to": "XXXXXXXXXXXXX"
}
```


> 💡 **Tip:** Keep your Device Key secure. Never share it publicly.
