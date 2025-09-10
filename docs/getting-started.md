---
title: Getting Started with Rapiwa
sidebar_label: Getting Started
---

# Getting Started with Rapiwa – WhatsApp Messaging API

Learn how to set up your **Rapiwa** account and start sending WhatsApp messages in just a few minutes.  
This guide covers **Account Creation**, **Device Setup**, **API Key Retrieval**, And **Sending Your First Message**.

---

## Introduction
Welcome to **Rapiwa** – your reliable WhatsApp API platform.  
With Rapiwa, you can send and receive WhatsApp messages using a simple, secure, and developer-friendly **REST API**.

By the end of this guide, you’ll:
- Have a connected WhatsApp session.  
- Get your **API Key**.  
- Send your first WhatsApp message.  

---

## Step 1: Create an Account
1. Go to the [Login page](https://app.rapiwa.com/login).  
2. Enter your **WhatsApp number** to register.  
3. Verify using the **OTP** sent to your WhatsApp.  
4. Once verified, log in to access your **dashboard**.

---

## Step 2: Create Your First WhatsApp Session
1. **Log in to your dashboard**  
   Go to [app.rapiwa.com/client/dashboard](https://app.rapiwa.com/client/dashboard).  
2. **Open the Devices Page**  
   Navigate to the **Devices** section.  
3. **Create a New Devices**  
   Click **Manage**.  
4. **Scan the QR Code**  
   - Open WhatsApp on your phone.  
   - Go to **Settings → Linked Devices**.  
   - Tap **Link a Device** and scan the QR code.  
5. **Activate Your Session**  
   Once linked, your WhatsApp session will be active, and you’ll see your **API Key**.

> 💡 **Tip:** Store your API Key securely. Do not share it publicly.

---

## Step 3: Send Your First Message

**API Endpoint:**

```http
POST https://app.rapiwa.com/api/send-message
```

### Header

```http
Content-Type: application/json
Authorization: Bearer Your_API_Key
```

**Body:**

```http
{
  "number": "88017XXXXXXXX",
  "message_type": "text",
  "message": "Hello from Postman!"
}
```

**Response:**

```bash
{
    "success": true,
    "message_type": "text",
    "message_id": "XXXXXXXXXXXXXXXX",
    "to": "88017XXXXXXXX"
}
```
