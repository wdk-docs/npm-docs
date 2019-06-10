Transferring a package from a user account to another user account
===========================================================================================

As a package owner or maintainer, you can transfer ownership of a package you no longer wish to maintain to another trusted npm user on either the npm website or the command line.

Transferring a package from a user to an Org, or an Org to a user works differently than this process.

For more information on how npm support handles package name disputes between users, you can refer to npm’s package name dispute policy.

.. note:: If your package is scoped and private, the new package owner must also have a paid user account. It is possible to transfer ownership of user-scoped packages, however we don't recommend it because it can create some ownership confusion.

Transferring a package from a user account to another user account on the website
--------------------------------------------------------------------------------------

To transfer a package you own or maintain to another user, follow these steps:

1. Navigate to the package page for the package you want to transfer, replacing <your-package-name> with the name of your package: https://www.npmjs.com/package/<your-package-name>.
2. On the package Admin tab, under “Maintainers”, enter the npm username of the new maintainer.

.. figure:: https://docs.npmjs.com/assets/images/packages-and-modules/pkg-page-admin-tab-invite-maintainer.png
   :alt: package page admin tab showing text field to invite maintainers

1. Click “Invite.”
2. To remove yourself as a maintainer, under the maintainers list, click the “x” next to your username.

.. figure:: https://docs.npmjs.com/assets/images/packages-and-modules/pkg-page-admin-tab-maintainers-list.png
   :alt: package page admin tab listing two maintainers

Transferring a package from a user account to another user account on the command line
-----------------------------------------------------------------------------------------

To transfer a package to another npm user using the CLI, run the npm owner add and rm commands in order, replacing <their-username> with the other user’s npm username, <your-username> with your npm username, and <package-name> with the package you want to transfer::

    npm owner add npm <their-username> <package-name>
    npm owner rm <your-username> <package-name>

If you have two-factor authentication enabled for writes, add a one-time password to the command, --otp=123456 (where 123456 is the code from your authenticator application).

.. code-block:: sh

    npm owner add npm <their-username> <package-name> --otp=123456
    npm owner rm <your-username> <package-name> --otp=123456
