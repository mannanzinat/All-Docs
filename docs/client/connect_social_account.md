---
title:   Facebook
sidebar_label:    Facebook
---

# Step1 Create Facebook Developer App
To setup **Whatsapp Feautre** follow the procedures…


- Go to **developer.facebook.com** &  login with **Meta Account**
- Then go to **Create App option** and create a **new app**

![SocialVibe](../assets/screenshots/create_app_1.png)

- Select **Other Option** and click **next**

![SocialVibe](../assets/screenshots/create_app_2.png)

- Select **Business** from **App Type**

![SocialVibe](../assets/screenshots/create_app_3.png)

- Provide **an unique name** for the **App**

![SocialVibe](../assets/screenshots/create_app_4.png)

- Go to **app dashboard** and select **whatsapp** for the **integration**. Then select **whatsapp API** settings.

![SocialVibe](../assets/screenshots/create_app_5.png)

- From **API Settings** you can get **temporary access token**,**Phone Number ID** and **Whatsapp Business Accout ID**. These credentials are essential for next step.

![SocialVibe](../assets/screenshots/create_app_6.png)


# Step2 Connect Webhook
To setup **Webhook** with **Whatsapp API credentials**  follow the procedures…


- Go to **Client Module** &  click **Settings**
- Then paste **Token**,**Phone Number ID** and **Whatsapp Business Account ID**. After completing the setup, you can access whatsapp features

![SocialVibe](../assets/screenshots/webhook_access_token.png)

![SocialVibe](../assets/screenshots/whatsapp_2.png)

# Step3 Create Permanent Access Token
To setup **Permanent Token** instead of **temporary token** follow the procedures…


- Go to **business.facebook.com** &  go to your **app**.
- Create a **system user** for the app

![SocialVibe](../assets/screenshots/permanent_token_1.png)

- From **Accounts**->**Apps**->**Assign People** the correct rights.

![SocialVibe](../assets/screenshots/permanent_token_2.png)

- After giving rights add the people into the **app**.

![SocialVibe](../assets/screenshots/permanent_token_3.png) 

- From next window select time expiration to **never** and select **whatsapp_business_management** and **whatsapp_business_rights**.
- New **permanent token** will be generated.

![SocialVibe](../assets/screenshots/permanent_token_4.png)

