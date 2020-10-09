# Web Security

### Reading List:

##### [Why do we need HTTPS](https://howhttps.works/why-do-we-need-https/)
##### [.NET OWASP Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/DotNet_Security_Cheat_Sheet.html)
##### [Top 10 OWASP for Core](https://dotnetcoretutorials.com/2017/10/16/owasp-top-10-asp-net-core-broken-authentication-session-management/)
##### [GDPR](https://www.microsoft.com/en-us/trust-center/privacy/gdpr-overview?&OCID=AID641639_SEM_CBaJdkAr&msclkid=69e6e33dba521b93d7d9b9c7e8f92223)

---

### Why do we need HTTPS

1. Privacy
2. Integrity
3. Identification

**Privacy**
* Privacy means that no one can eavesdrop on your content, such as messages and passwords.
* The green padlock on the URL bar of the browser tells us that the messages are encrypted and our privacy is protected.

**Integrity**
* Unencrypted messages are open to a 'man-in-the-middle' attack, where a 3rd party intecepts the message and maliciously updates it. 
* Integrity means that the message is not manipulated on the way to its destination.

**Identification**
* Identification means that we can check from where a message was sent. A digital signature attached to a message can identify the sender.
* When browsing the web, identification means that the site that you are visiting is indeed the one you think it is.
* HTTPS, via SSL certificates, ensures you are connected exactly with the receiver you would expect.

