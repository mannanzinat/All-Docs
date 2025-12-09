---
title: Send Contact Message
sidebar_label: Messages
---

## Send Contact Messages

This endpoint enables you to deliver contact cards to a WhatsApp user by specifying their phone number. It supports sending a structured contact message containing the recipient’s name and phone number.

---

### Parameters

| Name              | Type   | Required | Description                                                                             |
|-------------------|--------|----------|-----------------------------------------------------------------------------            |
| `number`          | string | Yes      | The recipient’s phone number. Any format is accepted (digits are extracted internally). |
| `message_type`    | string | Yes      | Type of message being sent. For this endpoint, use `contact`.                           |
| `contact_name`    | string | Yes      | Full name of the contact to be shared.                                                  |
| `contact_number`  | string | Yes      | Phone number of the contact to be shared.                                               |

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
  "number": "88017XXXXXXXXX",
  "message_type": "contact",
  "contact_name": "Golam Rabbi",
  "contact_number": "88017XXXXXXXXXX"
}
```

###**Response:**


```bash
{
    "success": true,
    "message_type": "contact",
    "message_id": "3EB0FAC204D805F0E22293",
    "to": "XXXXXXXXXXXXX"
}
```


> 💡 **Tip:** Keep your Device Key secure. Never share it publicly.
