Using private packages in a CI/CD workflow
==================================================================

You can use authentication tokens to test private npm packages with continuous integration (CI) servers, or deploy them to continuous deployment (CD) servers.

Overview§
Create a new authentication token
Set the token as an environment variable on the CI/CD server
Create and check in a project-specific .npmrc file
Create a new authentication token§
Create a new authentication token that will be used only to access npm packages from a CI/CD server.

Continuous integration§
By default, npm token create will generate a token with both read and write permissions. When generating a token for use in a continuous integration environment, we recommend creating a read-only token:

npm token create --read-only
For more information on creating authentication tokens, including CIDR-whitelisted tokens, see “Creating an authentication token”.

Continuous deployment§
Since continuous deployment environments usually involve the creation of a deploy artifact, the token likely will need read and write permissions, which are granted with the standard token creation command:

npm token create
.. note:: For increased security, we recommend generated a CIDR-whitelisted token that can only be used from a certain IP address range. You can use a CIDR whitelist with a read and publish token or a read-only token: npm token create --cidr=[list] npm token create --read-only --cidr=[list] Example: npm token create --cidr=192.0.2.0/24 For more information, see "Creating and viewing authentication tokens".
Set the token as an environment variable on the CI/CD server§
Set your token as an environment variable on the CI/CD server and your development machine. In OSX or Linux, add this line to your ~/.profile, replacing the example token with your own:

export NPM_TOKEN="00000000-0000-0000-0000-000000000000"
and then refresh your environment variables:

source ~/.profile
Create and check in a project-specific .npmrc file§
Use a project-specific .npmrc file with a variable for your token to securely authenticate your CI/CD server with npm.

In the root directory of your project, create a custom .npmrc file with the following contents:
//registry.npmjs.org/:_authToken=${NPM_TOKEN}
Check in the .npmrc file.
