---
title:   Instagram
sidebar_label:    Instagram
---

# Instagram Platform Configuration in SocialVibe

**NOTE:** Instagram and Facebook can use the same app (no need to create two separate apps).

## Steps to Configure:

1. Navigate to the **Platforms** section in the SocialVibe dashboard and locate the Facebook platform in the list.
2. Click on the **Settings** button (settings icon) under the "Options" column for the Facebook platform.
3. A modal titled **Update Configuration** will appear, displaying the following fields:
  - **Client ID**: Enter the Client ID from your Facebook developer account.
  - **Client Secret**: Enter the Client Secret from your Facebook developer account.
  - **App Version**: Specify the API version (e.g., v21.0).
  - **Graph API URL**: The default URL is `https://graph.facebook.com`.
  - **Group URL**: The default URL is `https://www.facebook.com/groups`.
  - **Callback URL**: Copy this URL using the copy button provided and paste it into your Facebook app's configuration in the Facebook Developer account.

4. Once you have successfully created the app in your Meta Developer account, proceed to add a new product:
  - Navigate to the **Menu** options in the Meta Developer account.
  - Select **Instagram** and click on the **Set Up** button.
  - Follow the subsequent steps to complete the setup process.

---

## API Setup for Instagram Business Login

Follow these steps to set up the Instagram API for Business Login in your Meta Developer account. This process allows you to use the Instagram API to create, publish, and manage content, interact with users, and moderate comments.

### Steps for API Setup:

1. **Generate Access Tokens:**
  - Add an Instagram account to generate access tokens and set up webhook subscriptions.
  - Click on the **Add Account** button to link your Instagram account.

2. **Configure Webhooks:**
  - Set up a custom webhook URL or use services that help you create an endpoint.
  - Ensure the app mode is set to **Live** to receive webhooks.
  - Click the **Configure** button to set this up.

3. **Set Up Instagram Business Login:**
  - Provide a secure way for businesses to grant your app permissions to access data using Instagram Business Login.
  - Click the **Set Up** button to configure this.

4. **Complete App Review:**
  - To access live data, your app must successfully complete the app review process.
  - Go through the review to request advanced access to Instagram permissions.
  - Submit your app for review when you are ready.

---

### Important Information:

- **Instagram App Name:** SocialVibe-IG
- **Instagram App ID:** 605508678636718
- **Instagram App Secret:** [Hidden for security]

For more details, refer to the [Meta Developer documentation](https://developers.facebook.com/docs/instagram-api/).
