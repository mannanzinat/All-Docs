---
title:   Facebook
sidebar_label:    Facebook
---
# Facebook Platform Configuration in SocialVibe

To integrate your Facebook account with SocialVibe, follow the steps outlined below:

## 1. Configure the Facebook Platform in SocialVibe

- **Access the SocialVibe Dashboard:**
  - Navigate to the **Platforms** section.
  - Locate the **Facebook** platform in the list.

- **Open Facebook Platform Settings:**
  - Click on the **Settings** button (represented by a settings icon) under the "Options" column for the Facebook platform.

- **Update Configuration Modal:**
  - A modal titled **Update Configuration** will appear, presenting the following fields:
    - **Client ID:** Enter the Client ID from your Facebook developer account.
    - **Client Secret:** Enter the Client Secret from your Facebook developer account.
    - **App Version:** Specify the API version (e.g., v21.0).
    - **Graph API URL:** The default URL is `https://graph.facebook.com`.
    - **Group URL:** The default URL is `https://www.facebook.com/groups`.
    - **Callback URL:** Use the provided copy button to copy this URL and paste it into your Facebook app's configuration in the Facebook Developer account.

## 2. Create a Facebook App

- **Log in to Facebook Developers:**
  - Visit the [Facebook Developers website](https://developers.facebook.com/) and log in to your account.

- **Initiate App Creation:**
  - Click on **My Apps** and select **Create App**.

- **Provide App Details:**
  - Enter your **App Name** and a valid email address.

- **Select App Type:**
  - Choose **Other**.
  - Then, select **Business** as the app type.

- **Associate Verified Business (if applicable):**
  - If you have a verified business, select it during this step.

- **Complete App Creation:**
  - After creating the app, you'll be directed to the Facebook Developer dashboard.

- **Set Up Login for Business:**
  - Configure a redirect URI back to the application. The callback URI can be found in the Accounts Config modal in SocialVibe.

## 3. Configure OAuth2 Redirect URIs for SocialVibe

- **Purpose of OAuth2 Redirect URI:**
  - This URI is where Facebook will redirect users after they attempt to log in or authenticate their social accounts.

- **Required Callback URLs:**
  - **For Login:**
    - `https://your-hosted-domain.com/login/facebook/callback`
  - **For Social Account Connectivity:**
    - `https://your-hosted-domain.com/account/facebook/callback?medium=facebook`

- **Examples Based on Environment:**
  - **Production Server:**
    - Use the URLs exactly as provided above, replacing `your-hosted-domain.com` with your actual domain.
  - **Local Development:**
    - Replace the base URL with `http://localhost:4200`. For example:
      - **Login Callback:** `http://localhost:4200/login/facebook/callback`
      - **Social Account Connectivity Callback:** `http://localhost:4200/account/facebook/callback?medium=facebook`

## 4. Request Advanced Permissions for Facebook Integration

- **Purpose:**
  - To enable advanced functionality in SocialVibe, such as managing pages, retrieving insights, and handling posts on your behalf.

- **Required Permissions (Scopes):**
  - In your Facebook App, navigate to the **Advanced Permission** section and request access for the following scopes:
    - `pages_show_list`
    - `business_management`
    - `pages_manage_posts`
    - `pages_manage_engagement`
    - `pages_read_engagement`
    - `read_insights`

## 5. Retrieve App Credentials and Finalize Configuration

- **Access App Settings:**
  - Go to **App Settings** > **Basic** in the Facebook Developer dashboard.

- **Obtain App ID and App Secret:**
  - Here, you'll find the **App ID** (Client ID) and **App Secret** (Client Secret).

- **Provide Required URLs:**
  - Ensure that you've provided the **App Domain**, **Privacy Policy URL**, and **Terms of Service URL**. These are mandatory for going live.

- **Finalize SocialVibe Configuration:**
  - Copy the App ID and App Secret, then paste them into the SocialVibe account configuration modal and save the settings.

## 6. Submit App for Review and Go Live

- **Meta Review:**
  - Once your app has been reviewed by Meta and all information has been provided correctly, you can proceed to the next step.

- **Switch to Live Mode:**
  - Toggle your app's status from **Development** to **Live** to make it publicly accessible.

By following these steps, you'll successfully integrate your Facebook account with SocialVibe, enabling seamless social media management and enhanced platform capabilities.
