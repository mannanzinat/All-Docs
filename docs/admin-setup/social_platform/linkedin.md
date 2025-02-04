---
title:   Linkedin
sidebar_label:    Linkedin
---
# LinkedIn Platform Configuration

Follow these steps to create and configure a LinkedIn developer app for integrating **SocialVibe** with LinkedIn pages.

## Step 1: Create a LinkedIn Developer App

1. Go to the [LinkedIn Developer Portal](https://developer.linkedin.com/) and log in to your account.
2. Click on the **My Apps** button in the top-right corner, as highlighted in the screenshot.
3. Click **Create App** and fill in the required fields:
  - **App Name**: Enter a suitable name for your app.
  - **LinkedIn Page**: Provide your company's LinkedIn page URL (e.g., `https://www.linkedin.com/company/your-company-name/`).
  - **Privacy Policy URL**: Provide a valid URL for your privacy policy (e.g., `https://yourwebsite.com/privacy-policy`).
  - **App Logo**: Upload a logo for your app (minimum dimensions: 100px).
  - **Legal Agreement**: Check the box to agree to LinkedIn's API Terms of Use.

4. Click **Create App** to complete the creation process.

## Step 2: Add Products

1. Navigate to the **Products** tab of your app.
2. Add the following products:
  - **Share on LinkedIn**: Enables sharing content on LinkedIn.
  - **Sign In with LinkedIn**: Allows authentication using LinkedIn credentials.

   If additional products like the Advertising API are needed, request access from LinkedIn.

## Step 3: Configure Authentication

1. Navigate to the **Auth** tab of your app.
2. Copy the following details:
  - **Client ID**: Unique identifier for your app.
  - **Client Secret**: Secure key for authentication. You can generate a new one if needed.
3. Set the **Authorized Redirect URLs** for your app to:
   ```
   https://socialvibe.spagreen.net/account/linkedin/callback
   ```
4. Save the changes.

## Step 4: Finalize the Setup

1. Ensure all settings are correctly configured, and the app status is set to **Live**.
2. Use the **Client ID**, **Client Secret**, and **Redirect URL** to integrate SocialVibe with LinkedIn through the SocialVibe platform.

## Setup SocialVibe LinkedIn Configuration Info

Provide all the necessary fields from the LinkedIn Developer account's created app in the SocialVibe platform.

For more details, refer to the [official LinkedIn Developer Documentation](https://docs.microsoft.com/linkedin/).
