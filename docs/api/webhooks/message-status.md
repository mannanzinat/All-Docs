# Webhook for Message Status

The Message Status webhook provides real-time updates on the delivery status of your messages. When the status of a sent message changes (e.g., from 'sent' to 'delivered' or 'read'), a notification is sent to your configured webhook URL.

## Webhook Payload

The webhook will send a `POST` request with a JSON payload to your specified URL. The payload contains the following parameters:

| Parameter    | Type   | Description                                         |
|--------------|--------|-----------------------------------------------------|
| `session_id` | string | The ID of the WhatsApp session.                     |
| `message_id` | string | The unique ID of the message.                       |
| `status`     | string | The new status of the message. Possible values are: `sent`, `delivered`, `read`. |

## Example Payload

Here is an example of the JSON payload you would receive:

```json
{
  "session_id": "XXXXXXXXXXXXXXXXX",
  "message_id": "3EB0BDC38AA36A7FD56ADD",
  "status": "read"
}
```

## Status Types

- **sent**: The message has been successfully sent from the server.
- **delivered**: The message has been delivered to the recipient's device.
- **read**: The recipient has read the message.
