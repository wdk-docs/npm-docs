Configuring an authentication provider
=============================================

Note: To avoid being locked out of your instance, you must connect your npm Enterprise admin account to your SSO account immediately after configuring an authentication provider. If you are locked out of your instance, contact npm Enterprise Support at enterprise@npmjs.com.
As an Enterprise admin, you can configure your instance to use single sign-on (SSO) authentication through any external authentication provider that implements OpendID Connect Core and OpendID Connect Discovery, such as Auth0, Azure Active Directory, Okta, and Google.

Log in to your Enterprise instance using your temporary username and password.
In the upper right corner of the page, click your profile picture, then click Site Administration. drop-down with site administration choice
Click “settings”. admin panel settings button
On the Settings page, click “Configure Single Sign-On”. configure single sign on button
On the Single Sign-On configuration page, enter your SSO application settings:
Domain: enter the base domain, without the https:// prefix
Client ID
Client Secret fields for sso settings form
Click Save. sso settings form save button
On your SSO provider application website, enter your npm Enterprise instance callback URL: www.<company-name>.npme.io/sso/callback.
To connect your npm Enterprise admin account to your SSO account, visit https://<company-name>.npme.io/login/via/1.
Removing users from your authentication provider§
When you remove a user from your authentication provider, we also recommend deactivating them in your instance.

