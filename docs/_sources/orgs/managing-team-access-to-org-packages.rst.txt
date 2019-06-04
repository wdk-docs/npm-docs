Managing team access to Org packages
====================================================================

As an Org owner or team admin, you can add or remove package access to or from teams in your Org.

Adding package access to a team on the web§
Log in to npm with your user account. npm login dialog with username and password fields left blank
In the upper right corner of the page, click your profile picture, then click Profile Settings. npm avatar menu with selector over profile settings list item
In the left sidebar, click the name of your Org. example org selected in organizations list
On the Org settings page, click Teams. teams tab
Beside the team to which you want to add package access, click Packages. packages button
On the “Add Packages” page, in the “Package” field, type the name of the package and select from the dropdown menu. package name search field and dropdown
Click + Add Existing Package. add existing package button
Beside the package name, click read or read/write to set the team permissions for the package. package permissions selector with read and write selected
Adding package access to a team using the CLI§
As an Org owner or team admin, you can use the the CLI access command to add package access to a team on the command line:

npm access grant <read-only|read-write> <org:team> [<package>]
For more information, see “npm-access”.

Removing package access from a team on the web§
Log in to npm with your user account. npm login dialog with username and password fields left blank
In the upper right corner of the page, click your profile picture, then click Profile Settings. npm avatar menu with selector over profile settings list item
In the left sidebar, click the name of your Org. example org selected in organizations list
On the Org settings page, click Teams. teams tab
Beside the team from which you want to remove package access, click Packages. packages button
Beside the name of the package from which you want to remove access, click x. x button
Removing package access from a team using the CLI§
As an Org owner or team admin, you can also use the the CLI access command to revoke package access from a team on the command line:

npm access revoke <org:team> [<package>]
For more information, see “npm-access”.

Changing package access for a team on the web§
Log in to npm with your user account. npm login dialog with username and password fields left blank
In the upper right corner of the page, click your profile picture, then click Profile Settings. npm avatar menu with selector over profile settings list item
In the left sidebar, click the name of your Org. example org selected in organizations list
On the Org settings page, click Teams. teams tab
Beside the team from which you want to remove package access, click Packages. packages button
Beside the package name, click read or read/write to set the team permissions for the package. package permissions selector with read selected
Changing package access for a team from the CLI§
As an Org owner or team admin, you can change package access for a team from the command line:

npm access
For more information, see the npm-access CLI documentation.
