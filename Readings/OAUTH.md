# OAUTH

### Reading List:

##### [OAUTH MSFT Docs](https://docs.microsoft.com/en-us/aspnet/core/security/authentication/social/?view=aspnetcore-2.1&tabs=visual-studio)
##### [OAUTH](https://www.jerriepelser.com/blog/authenticate-oauth-aspnet-core-2/)

---

#### Facebook, Google, and external provider authentication in ASP.NET Core

* This tutorial shows how to enable users to sign into your app, using OAuth 2.0 with credentials from external authentication providers. 

* Enabling users to sign in with their existing credentials:

	* Is more convenient for the users.
	* Shifts many of the complexities of managing the sign-in process onto a third party.


#### Forward request information with a proxy or load balancer

* If the app is deployed behind a proxy server or load balancer, some of the original request information might be forwarded to the app in request headers. 

* This information usually includes the secure request scheme (https), host, and client IP address. 


#### Use SecretManager to store tokens assigned by login providers

* Social login providers assign Application Id and Application Secret tokens during the registration process. The exact token names vary by provider.

* These tokens represent the credentials your app uses to access their API. The tokens constitute the "secrets" that can be linked to your app configuration with the help of Secret Manager. 

#### Setup login providers required by your application

Instructions on how to configure your application to use the respective providers:

* [Facebook](https://docs.microsoft.com/en-us/aspnet/core/security/authentication/social/facebook-logins?view=aspnetcore-3.1&viewFallbackFrom=aspnetcore-2.1)
* [Twitter](https://docs.microsoft.com/en-us/aspnet/core/security/authentication/social/twitter-logins?view=aspnetcore-3.1&viewFallbackFrom=aspnetcore-2.1)
* [Google](https://docs.microsoft.com/en-us/aspnet/core/security/authentication/social/google-logins?view=aspnetcore-2.1) 
* [Microsoft](https://docs.microsoft.com/en-us/aspnet/core/security/authentication/social/microsoft-logins?view=aspnetcore-3.1&viewFallbackFrom=aspnetcore-2.1) 
* [Other providers](https://docs.microsoft.com/en-us/aspnet/core/security/authentication/social/other-logins?view=aspnetcore-2.1) 

#### Multiple authentication providers

When the app requires multiple providers, chain the provider extension methods behind AddAuthentication:

```
services.AddAuthentication()
    .AddMicrosoftAccount(microsoftOptions => { ... })
    .AddGoogle(googleOptions => { ... })
    .AddTwitter(twitterOptions => { ... })
    .AddFacebook(facebookOptions => { ... });
```

#### Optionally set password

* When you register with an external login provider, you don't have a password registered with the app. This alleviates you from creating and remembering a password for the site, but it also makes you dependent on the external login provider.

* You can also create a password and sign in using your email that you set during the sign in process with external providers.
