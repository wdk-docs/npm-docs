Requiring 2FA for package publishing and settings modification
===========================================================================================

To protect your packages, as a package publisher, you can require everyone who has write access to a package to provide a one-time password in addition to their login token when they publish the package to the registry or modify package settings.

To publish or modify a package with the two factor authentication (2FA) setting enabled, a publisher must have 2FA enabled on their user account with “Authorization and Publishing” selected. For more information, see “Configuring two-factor authentication”.

Note: Currently, publishing a package with 2FA enabled on CI is not possible. For more secure CI publishing, enable 2FA on the npm account used for CI, and select "Authorization" only, and create a CIDR-restricted token for CI by following the steps in "Creating and viewing authentication tokens".

Enabling two-factor authentication for package publishing
--------------------------------------------------------------------------

Log in to npm with your user account. npm login dialog with username and password fields left blank
Navigate to the package on which you want to require a second factor to publish or modify settings.
Click Admin. admin tab on package page
Under “Package Access”, select “Require Two Factor Authentication to publish or modify settings” require two factor authentication to publish or modify settings checkbox selected
Click Update Package Settings. update package settings button

Disabling two-factor authentication for package publishing
--------------------------------------------------------------------------
Log in to npm with your user account. npm login dialog with username and password fields left blank
Navigate to the package on which you want to remove the requirement for a second factor to publish or modify settings.
Click Admin. admin tab on package page
Under “Package Access”, deselect “Require Two Factor Authentication to publish or modify settings” require two factor authentication to publish or modify settings checkbox deselected
Click Update Package Settings. update package settings button
