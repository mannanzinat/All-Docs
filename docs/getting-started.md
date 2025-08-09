---
title: Getting Started with Rapiwa
sidebar_label: Getting Started
---

# Introduction

# Getting Started with Rapiwa – WhatsApp Messaging API

Learn how to quickly set up your **Rapiwa** account and start sending WhatsApp messages in minutes.  
This guide covers account creation, token generation, sending your first message, and tracking delivery using our developer-friendly REST API.

---

## Introduction
Welcome to **Rapiwa** – your reliable WhatsApp API platform.  
This guide will walk you through the steps to set up and start sending messages using our powerful API.  
It's quick, secure, and developer-friendly.

---

## Step 1: Create an Account
1. Go to the [registration page](https://rapiwa.com/register).  
2. Fill in your details and verify your email address.  
3. Once verified, log in to access your dashboard.

---

## Step 2: Create Your First WhatsApp Session
1. **Log In to Your Dashboard**  
   Access your account at [rapiwa.com/dashboard](https://rapiwa.com/client/dashboard).  
2. **Navigate to the Sessions Section**  
   In the dashboard, go to the **Sessions** tab.  
3. **Create a New Session**  
   Click **Create New Session**.  
4. **Scan the QR Code**  
   - Open WhatsApp on your phone.  
   - Go to **Settings → Linked Devices**.  
   - Scan the QR code to link your WhatsApp account.  
5. **Session Activation**  
   Once scanned, your session will be connected, and you can copy your API key.

> 📘 **Tip:** For a more advanced walkthrough, check out the [detailed guide here](https://rapiwa.com/help-center).

---

## Step 3: Send Your First Message

**API Endpoint:**

```http
POST https://www.rapiwa.com/session/{API_Key}/send-message
```

**Body:**

```bash
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
    "message_id": "3EB0C9C1719F058FFABB63",
    "to": "88017XXXXXXXX@s.whatsapp.net"
}
```
