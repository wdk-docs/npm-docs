Changing package visibility
===================================

You can change the visibility of a scoped package from the website or command line.

You must be the owner of the user account or Org that owns the package in order to change package visibility.

For more information about package visibility, see “Package scope, access level, and visibility”.

Note: Adding a scope to an unscoped package will not make it private. If you want to make a unscoped package private, contact npm Support.
Making a public package private
-------------------------------------------------------

Note: Making a package private requires a paid user account or Org. To sign up for a paid user or Org, go to https://www.npmjs.com/settings/account-name/billing, replacing account-name with the name of your npm user account or Org.
If you want to restrict access and visibility for a public package you own, you can make the package private. When you make a package private, it will be removed from the website within a few minutes of the change.

Website
-------------------------------------------------------

On the npm website, go to the package page.
On the package page, click Admin.
Under “Package Access”, select “Is Package Private?”
Click Update package settings.
Command line
-------------------------------------------------------

To make a public package private on the command line, run the following command, replacing <package-name> with the name of your package:

npm access restricted <package-name>
For more information, see the npm access documentation.

Making a private package public
-------------------------------------------------------

Note: When you make a private package public, the package will be visible to and downloadable by all npm users.
Website
-------------------------------------------------------

On the npm website, go to the package page.
On the package page, click Admin.
Under “Package Access”, deselect “Is Package Private?”
Click Update package settings.
Command line
-------------------------------------------------------

To make a private package public on the command line, run the following command, replacing <package-name> with the name of your package:

npm access public <package-name>
For more information, see the npm access CLI documentation.

