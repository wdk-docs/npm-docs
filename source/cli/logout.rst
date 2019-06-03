npm-logout
============================================================================================

Log out of the registry

SYNOPSIS
-------------------

.. program:: npm

.. option:: logout

npm logout [--registry=<url>] [--scope=<@scope>]

DESCRIPTION
-------------------

When logged into a registry that supports token-based authentication, tell the server to end this token’s session. This will invalidate the token everywhere you’re using it, not just for the current environment.

When logged into a legacy registry that uses username and password authentication, this will clear the credentials in your user configuration. In this case, it will only affect the current environment.

If --scope is provided, this will find the credentials for the registry connected to that scope, if set.

CONFIGURATION
-------------------


registry


Default: https://registry.npmjs.org/

The base URL of the npm package registry. If scope is also specified, it takes precedence.

scope

Default: The scope of your current project, if any, otherwise none.

If specified, you will be logged out of the specified scope. See npm-scope.

npm logout --scope=@myco

SEE ALSO
-------------------

- npm-adduser
- npm-registry
- npm-config
- npm-config
- npmrc
- npm-whoami
