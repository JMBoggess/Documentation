# Authentication with Azure Active Directory
Azure provides built-in support for simplifying authentication using Microsoft Entra ID (Azure AD)

[Configure your App Service or Azure Functions app to use Azure AD sign-in](https://learn.microsoft.com/en-us/azure/app-service/configure-authentication-provider-aad?tabs=workforce-tenant)

The above article walks step-by-step setup of the Azure Web App and App Registration (in Microsoft Entra ID)

## HTTP Response Headers
The App Services passes authentication objects in the response headers to the application

| Header | Description |
| --- | --- |
| X-Ms-Client-Principal-Name |  jboggess@greymatterconcepts.net	
X-Ms-Client-Principal-Id	b18769e5-25c7-49c6-a386-1d686ccbedb6	
X-Ms-Client-Principal-Idp	aad	
X-Ms-Client-Principal	long token-like string	
X-Ms-Token-Aad-Access-Token	long token string	
X-Ms-Token-Aad-Expires-On	2023-10-03T15:08:43.6226525Z	
X-Ms-Token-Aad-Id-Token	long token-like string

References:
- [Work with user identities in Azure App Service authentication](https://learn.microsoft.com/en-us/azure/app-service/configure-authentication-user-identities)

## Enable Refresh Tokens
The above, by default, does not create refresh tokens
