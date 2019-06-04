Logging in to an npm Enterprise registry from the command line
===============================================================================

The steps for logging in to your company’s npm Enterprise registry will depend how you configured your npm registry settings.

- Logging in with your default registry set to your company’s npm Enterprise registry
- Logging in with npmrc
- Logging in with a scope configured to point to an npm Enterprise registry

Logging in with your default registry set to your company’s npm Enterprise registry
--------------------------------------------------------------------------------------------

On the command line, type the following command:

  .. code-block::

    npm login

When prompted, provide your SSO credentials.

Logging in with npmrc
--------------------------------------------------------------------------------------------

1. On the command line, switch to your npm Enterprise profile:

  .. code-block::

    npmrc work

2. Run the following command:

  .. code-block::

    npm login

3. When prompted, provide your SSO credentials.

Logging in with a scope configured to point to an npm Enterprise registry
--------------------------------------------------------------------------------------------

1. On the command line, type the following command:

  .. code-block::

    npm login --registry=https://registry.company-name.npme.io

2. When prompted, provide your SSO credentials.
