Transferring a package from a user account to an Org
===========================================================================================

As a package maintainer, you may want to move a package into an Org so that all members or everyone on a specific team, can publish to the package.

.. note:: If your package is private, the new package owner must also have a paid user account It is possible to transfer ownership of scoped packages, however we don't recommend it because it can create some ownership confusion.
Transferring packages between a user and an Org works slightly differently than transferring packages between users. There will be an extra step of adding the package to an Org team. The new maintainer or owner will also need to be the Org owner or team admin.

Transferring a package from a user account to an Org on the website
-------------------------------------------------------

To transfer a package you own or maintain to an Org, follow these steps:

Navigate to the package page for the package you want to transfer, replacing <your-package-name> with the name of your package: https://www.npmjs.com/package/<your-package-name>.
On the package Admin tab, under “Maintainers,” enter the npm username of the new maintainer.
package page admin tab showing text field to invite maintainers

Click “Invite.”
To remove yourself as a maintainer, under the maintainers list, click the “x” next to your username.
package page admin tab listing two maintainers

.. note:: Once this has been done, the Org owner or team admin who is now a maintainer on the package will need to add the package to an Org team.

Transferring a package from a user account to an Org on the command line
-------------------------------------------------------

To transfer a package to an Org using the CLI, on the command line, run the npm owner add and rm commands in order, replacing <their-username> with the npm username of the Org owner or team admin, and <your-username> with your npm username, and <package-name> with the package you want to transfer:

npm owner add npm <their-username> <package-name>
npm owner rm <your-username> <package-name>
If you have two-factor authentication enabled for writes, add a one-time password to the commands, --otp=123456 (where 123456 is the code from your authenticator application).

npm owner add npm <their-username> <package-name> --otp=123456
npm owner rm <your-username> <package-name> --otp=123456
.. note:: After this is done, the Org owner or team admin will be able to add the package to a team in their Org, using the access command.
