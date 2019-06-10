Creating and viewing authentication tokens
==================================================================

You can create and view authentication tokens from the website and command line interface (CLI).

Creating authentication tokens§
Creating tokens on the website§
In the upper right corner of the page, click your profile picture, then click Tokens. profile dropdown menu with tokens link selected
Click Create New Token. create new token button
Select the access level:
Read and Publish: Recommended for continuous deployment and other environments where a deploy artifact is created and published to npm.
Read Only: Recommended for continuous integration and other environments where a deploy artifact is not created. token access level radio buttons with read and publish selected
Click Create Token.
Copy the token from the top of page.
Creating tokens with the CLI§
You can create tokens with read and publish permissions, read-only permissions, and CIDR-whitelisted tokens with either read and publish or read-only permissions with the CLI.

Read and publish: The default setting for new tokens, and most permissive token type. Read and publish tokens allow installation, distribution, modification, publishing, and all rights that you have on your account.
Read-only: Tokens that allow installation and distribution only, but no publishing or other rights associated with your account.
CIDR-whitelisted Tokens that can be used from specified IPv4 address ranges. Specifying a CIDR whitelist for a token allows you to make any user or system using the token to be physically or remotely located within the specified IP address range.
To create a new token, on the command line, run:
npm token create for a read and publish token
npm token create --read-only for a read-only token
npm token create --cidr=[list] for a CIDR-restricted read and publish token. For example, npm token create --cidr=192.0.2.0/24
npm token create --read-only --cidr=[list] for a CIDR-restricted read-only token
When prompted, enter your password.
If you have enabled two-factor authentication, when prompted, enter a one-time password.
Copy the token from the token field in the command output.
CIDR-restricted token errors§
If the CIDR string you enter is invalid or in an inappropriate format, you will get an error similar to the one below:

npm ERR! CIDR whitelist contains invalid CIDR entry: X.X.X.X./YY,Z.Z.. . .
Make sure you are using a valid IPv4 range and try creating the token again.

Viewing tokens§
.. note:: You can only view a full token immediately after creation.
Viewing tokens on the website§
To view all tokens associated with your account, in the upper right corner of the page, click your profile picture, then click Tokens.

profile dropdown menu with tokens link selected

Viewing tokens on the CLI§
To view all tokens associated with your account, on the command line, run the following command:

npm token list
Token attributes§
id: Use the token ID to refer to the token in commands.
token: The first digits of the actual token.
create: Date the token was created.
readonly: If yes, indicates a read-only token. If no, indicates a token with both read and publish permissions.
CIDR whitelist: Restricts token use by IP address.
