About authentication tokens
==================================================================

.. note:: You must be using npm version 5.5.1 or greater to use authentication tokens.
An authentication token is a hexadecimal string that gives you the right to publish and access your modules. Whenever you log in to npm, we generate an authentication token for you.

You can also create an authentication token to give other tools (such as continuous integration testing environments) access to your npm packages. For example, Travis CI provides an environment variable that you can set to an npm token value, which gives Travis CI the ability to run npm as your npm user. When Travis CI runs, it will be able to complete npm tasks as you, including installing private packages you can access.

You can work with tokens from the web or the CLI, whichever is easiest. What you do in each environment will be reflected in the other environment.

npm token commands let you:

View tokens for easier tracking and management
Create new tokens, specifying read-only or full-permission
Limit access according to IP address ranges (CIDR)
Delete/revoke tokens
For more information on creating and viewing authentication tokens on the web and CLI, see “Creating and viewing authentication tokens”.
