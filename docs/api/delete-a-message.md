---
title: Delete a Message
sidebar_label: Messages
---

## Delete a Message

Deletes a specific message for everyone in the chat (if permitted by WhatsApp).

> **Note:** You can only delete messages that were sent by your own WhatsApp account, and within WhatsApp's allowed deletion timeframe (usually about 1 hour after sending).

---

### Parameters

| Name          | Type   | Required | Description                                                   |
|---------------|--------|----------|---------------------------------------------------------------|
| `number`      | string | Yes      | Recipient phone number in any format (digits only extracted internally). |
| `message_id`  | string | Yes      | ID of the message to be deleted. This ID is returned when the message was originally sent. |


### API Endpoint

```http
POST https://app.rapiwa.com/api/delete-message
```

### Header

```http
Content-Type: application/json
Authorization: Bearer Your_Device_Key
```

### Body

```http
{
  "number": "88017XXXXXXXXX",
  "message_id": "XXXXXXXXXXXXXXXXXXXXX"
}
```

###**Response:**


```bash
{
  "success": true,
  "message_id": "XXXXXXXXXXXXXXXXXXX"
}
```


> 💡 **Tip:** Keep your Device Key secure. Never share it publicly.
