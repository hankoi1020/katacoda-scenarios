## Introduction

Some as previous one, this plugin is also a security plugin, it provide different feature to protect the website as well.

It can prevent from these external attacks:

- **Brute force attack: It can limit the login attempts, block an ip if perform many too attempt with advance functions.** 
- **Spam: Anti-spam engine to protect the forms from spam**
- **Bot: It can apply reCAPTCHA on website to confirm action is perform by human**
- **Malicious script injection: Disable PHP upload**


## Installation

Go to Plugins > Add new and search WP Cerber, install and activate it.

![圖片](https://user-images.githubusercontent.com/74434769/141387473-6787f54e-786c-4135-8302-b647de8ec8a0.png)

After that, you may go in WP Cerber interface by this button in left hand side.

![圖片](https://user-images.githubusercontent.com/74434769/141547383-7e103087-34c1-4705-b9bd-f5136af8fcad.png)


## Security

Admin can find and configure these security function in the **Main Settings** page

**Login Security**
- **Limit login attempts** : Limit the number of login attempts within a period 
 ![圖片](https://user-images.githubusercontent.com/74434769/141588759-89caed28-580a-424c-bc2c-3272ab3e12c6.png)

- **Block IP address** : An ip will be blocked if the attempts more than the limit, user can set the blocking time
![圖片](https://user-images.githubusercontent.com/74434769/141590157-5f33ac31-7c86-4eb7-80a6-bf40eadd9643.png)


- **Mitigate aggressive attempts** : An ip will block longer time if lockout more than a number within a period
![圖片](https://user-images.githubusercontent.com/74434769/141592411-b618acd2-f7a9-4430-b697-5987cc6a67c4.png)
- **Sample of ip blocked case**
![圖片](https://user-images.githubusercontent.com/74434769/141579636-71754156-e295-43f3-93ff-242ea634cad0.png)
![圖片](https://user-images.githubusercontent.com/74434769/141579880-82b9e9ca-f8c9-4953-81c3-093835270986.png)

- **Proactive security rules** : This function provide some rules to have more way to block the attack proactively, those rules can protect user/admin account from brute force attack. 
![圖片](https://user-images.githubusercontent.com/74434769/141593855-2bbdb706-edfa-48e7-bff2-003237ab7dd7.png)


- **Hardening** : This function protect the user account and website. It prevent the username discovery to avoid user subject to attack. It also disable PHP script upload to prevent someone inject malicious php code into the website. Disable PHP error displaying prevent someone try to get server information from those error message.
![圖片](https://user-images.githubusercontent.com/74434769/141594426-315c2f93-b37f-4650-8263-c062e899395c.png)

- **Anti-spam** : In Anti-spam session, it has a function call Anti-Spam Engine to against spam. In Cerber anti-spam engine, it protect each form in website to prevent spam. In Comment processing, it can handle the spam once the spam detected.
![圖片](https://user-images.githubusercontent.com/74434769/141594747-755d5099-bbcd-4c76-af69-6f8891d62680.png)
![圖片](https://user-images.githubusercontent.com/74434769/141594759-8736ce85-cad8-4e69-ba31-87f2ab59a086.png)
  
- **Bot Detection** : This function included in the Anti-spam session, it provide ReCAPTCHA to protect form in website to prevent bot. It also has limit attempts to lockout a user who attempt more than a number within a period. You may go to Google to apply a site key in order to enable this function.
![圖片](https://user-images.githubusercontent.com/74434769/141595698-1dcee866-47a4-4012-a403-81660900b4a2.png)

- **Two-factor authentication** : In User Policies session, it provide Two-factor authentication function to protect user account.
![圖片](https://user-images.githubusercontent.com/74434769/141597298-49ebc6cf-35d1-42ca-986d-540cab135afa.png)

