---
title: About email notifications for pushes to your repository
intro: You can choose to automatically send email notifications to a specific email address when anyone pushes to the repository.
permissions: People with admin permissions in a repository can enable email notifications for pushes to your repository.
redirect_from:
  - /articles/managing-notifications-for-pushes-to-a-repository/
  - /articles/receiving-email-notifications-for-pushes-to-a-repository/
  - /articles/about-email-notifications-for-pushes-to-your-repository/
  - /github/receiving-notifications-about-activity-on-github/about-email-notifications-for-pushes-to-your-repository
versions:
  free-pro-team: '*'
  enterprise-server: '*'
---

{% if currentVersion != "free-pro-team@latest" %}{% data reusables.notifications.outbound_email_tip %}{% endif %}

Each email notification for a push to a repository lists the new commits and links to a diff containing just those commits. In the email notification you'll see:

- The name of the repository where the commit was made
- The branch a commit was made in
- The SHA1 of the commit, including a link to the diff in {% data variables.product.product_name %}
- The author of the commit
- The date when the commit was made
- The files that were changed as part of the commit
- The commit message

You can filter email notifications you receive for pushes to a repository. For more information, see {% if currentVersion == "free-pro-team@latest" or currentVersion ver_gt "enterprise-server@2.20" %}"[Configuring notifications](/github/managing-subscriptions-and-notifications-on-github/configuring-notifications#filtering-email-notifications){% else %}"[About notification emails](/github/receiving-notifications-about-activity-on-github/about-email-notifications)." You can also turn off email notifications for pushes. For more information, see "[Choosing the delivery method for your notifications](/enterprise/{{ currentVersion }}/user/github/receiving-notifications-about-activity-on-github/choosing-the-delivery-method-for-your-notifications){% endif %}."

### Enabling email notifications for pushes to your repository

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
{% data reusables.repositories.sidebar-notifications %}
5. Type up to two email addresses, separated by whitespace, where you'd like notifications to be sent. If you'd like to send emails to more than two accounts, set one of the email addresses to a group email address. ![Email address textbox](/assets/images/help/settings/email_services_addresses.png)
6. If you operate your own server, you can verify the integrity of emails via the **Secret** token. This token is sent with the email as the `Approved` header. If the `Approved` header matches the token you sent, you can trust that the email is from {% data variables.product.product_name %}. ![Email secret textbox](/assets/images/help/settings/email_services_token.png)
7. Optionally, select **Send from author** to have emails delivered using the committer's email address. Otherwise, emails are sent from {% data variables.notifications.no_reply_address %}. ![Email author checkbox](/assets/images/help/settings/email_services_author.png)
8. Click **Save settings**. ![Save settings button](/assets/images/help/settings/save_notification_settings.png)

### ??? ????????????
{% if currentVersion == "free-pro-team@latest" or currentVersion ver_gt "enterprise-server@2.20" %}
- "[About notifications](/github/managing-subscriptions-and-notifications-on-github/about-notifications)"
{% else %}
- "[About notifications](/enterprise/{{ currentVersion }}/user/github/receiving-notifications-about-activity-on-github/about-notifications)"
- "[Choosing the delivery method for your notifications](/enterprise/{{ currentVersion }}/user/github/receiving-notifications-about-activity-on-github/choosing-the-delivery-method-for-your-notifications)"
- "[About email notifications](/enterprise/{{ currentVersion }}/user/github/receiving-notifications-about-activity-on-github/about-email-notifications)"
- "[About web notifications](/enterprise/{{ currentVersion }}/user/github/receiving-notifications-about-activity-on-github/about-web-notifications)"{% endif %}
