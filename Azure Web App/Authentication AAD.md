# Authentication with Azure Active Directory
Azure provides built-in support for simplifying authentication using Microsoft Entra ID (Azure AD)

[Configure your App Service or Azure Functions app to use Azure AD sign-in](https://learn.microsoft.com/en-us/azure/app-service/configure-authentication-provider-aad?tabs=workforce-tenant)

The above article walks step-by-step setup of the Azure Web App and App Registration (in Microsoft Entra ID)

## HTTP Response Headers
The App Services passes authentication objects in the response headers to the application

| Header | Description |
| --- | --- |
| X-Ms-Client-Principal-Name |  Email |	
| X-Ms-Client-Principal-Id | Microsoft Entry Object ID |
| X-Ms-Client-Principal-Idp | aad |
| X-Ms-Client-Principal | |
| X-Ms-Token-Aad-Access-Token | |
| X-Ms-Token-Aad-Expires-On | 2023-10-03T15:08:43.6226525Z | 
| X-Ms-Token-Aad-Id-Token | |

References:
- [Work with user identities in Azure App Service authentication](https://learn.microsoft.com/en-us/azure/app-service/configure-authentication-user-identities)

## Enable Refresh Tokens
The above, by default, does not create refresh tokens
