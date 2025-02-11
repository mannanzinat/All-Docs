---
title: Configure email settings

sidebar_label:  Configure email settings
---

# Configure email settings

Yoori e-Commerce CMS supports **SMTP, SendGrid, MailGun, SendMail**

### Configure the SMTP system follow the steps below.

- Create an email from your server panel
- After creating an email account, go to ** Admin Panel-> System Setup-> Email settings.**
- Select **SMTP mail driver**
- **Attention** (*This email setting is a must to verify email to send news to the subscriber.*)
- Fill up the form as below:

![SocialVibe](../assets/screenshots/email_settings.png)

- **MAIL_HOST** – Email host e.g smtp.mailtrap.io
- **MAIL_PORT** – Outgoing email port e.g 2525 or 465
- **MAIL_USERNAME** – Outgoing email username
- **MAIL_PASSWORD** – Outgoing email password
- **MAIL_ENCRYPTION** – Default null other options tls and ssl
- **MAIL_FROM_ADDRESS** – The email address that sends emails (Your company address)
- **MAIL_FROM_NAME** – Your company name that appears on emails

:::info

At the same way we can configure **SendGrid**, **MailGun** mail driver.
:::
