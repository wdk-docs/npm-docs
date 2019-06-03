Managing your profile settings
===============================================================================

You can manage settings for your user account profile from the web or command line.

Managing user account profile settings from the web
From the web, you can change the following user profile settings:

Avatar
Password
Full name
GitHub user name
Twitter user name
Email address added to package metadata
Two-factor authentication status
Log in to npm with your user account. npm login dialog with username and password fields left blank
In the upper right corner of the page, click your profile picture, then click Profile Settings. npm avatar menu with selector over profile settings list item
Managing user account profile settings from the command line
Note: Your npm client must be version 5.5.1 or higher to change your account settings from the CLI. To update to the latest version of npm, on the command line, run npm install npm@latest -g
Viewing user account profile settings from the command line
To view your user profile settings from the CLI, on the command line, run the following command:

npm profile get
command line interface profile settings table

Updating user account profile settings from the command line
From the CLI, you can change the following properties for your user account:

email
two-factor auth
fullname
homepage
freenode
twitter
github
password
On the command line, type the following command, replacing property with the name of the property, and value with the new value:
  npm profile set <prop> <value>
When prompted, provide your current password.
If you have enabled two-factor authentication on your account, when prompted, enter a one-time password.
For more details, see the profile command line documentation.

Setting a password from the command line
On the command line, type the following command:
  npm profile set password
When prompted, provide your current password.
When prompted, type a new password.
To protect your account, when you reset your password from the command line, it must:
be longer than 7 characters
not contain part of your username
not be on this list of common passwords
not be in the "Have I Been Pwned" breach database
Configuring two-factor authentication from the command line
Enabling two-factor authentication on your account helps protect against unauthorized access to your account and packages.

To enable, configure, and disable two-factor authentication from the command line, see “Configuring two-factor authentication”.
