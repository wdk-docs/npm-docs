Logging in to an npm Enterprise registry from the command line
===============================================================================

The steps for logging in to your company’s npm Enterprise registry will depend how you configured your npm registry settings.

Logging in with your default registry set to your company’s npm Enterprise registry
Logging in with npmrc
Logging in with a scope configured to point to an npm Enterprise registry
Logging in with your default registry set to your company’s npm Enterprise registry
On the command line, type the following command:
 npm login
When prompted, provide your SSO credentials.
Logging in with npmrc
On the command line, switch to your npm Enterprise profile:
 npmrc work
Run the following command:
 npm login
When prompted, provide your SSO credentials.
Logging in with a scope configured to point to an npm Enterprise registry
On the command line, type the following command:
 npm login --registry=https://registry.company-name.npme.io
When prompted, provide your SSO credentials.
