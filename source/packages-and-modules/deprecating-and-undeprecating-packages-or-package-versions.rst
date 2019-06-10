Deprecating and undeprecating packages or package versions
===========================================================================================

If you no longer wish to maintain a package, or if you would like to encourage users to update to a new or different version, you can :option:`npm deprecate` it.
Deprecating a package or version will print a message to the terminal when a user installs it.

A deprecation warning or message can say anything. You may wish to include a message encouraging users to update to a specific version, or an alternate, supported package.

.. note:: We strongly recommend deprecating packages or package versions instead of `unpublishing <https://docs.npmjs.com/unpublishing-packages-from-the-registry>`_ them, because unpublishing removes a package from the registry entirely, meaning anyone who relied on it will no longer be able to use it, with no warning.

Deprecating an entire package or a single version of a package
-----------------------------------------------------------------

Deprecating an entire package
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Deprecating an entire package will remove it from search results on the npm website, and a deprecation message will also be displayed on the package page.

.. figure:: https://docs.npmjs.com/assets/images/packages-and-modules/deprecate-package.png
   :alt: deprecation message saying package no longer supported use at your own risk

To deprecate an entire package, run the following command, replacing <package-name> with the name of your package, and "<message>" with your deprecation message::

    npm deprecate <package-name> "<message>"

If you have enabled `two-factor authentication <https://docs.npmjs.com/about-two-factor-authentication>`_, add a one-time password to the command, --otp=123456 (where 123456 is the code from your authenticator app).

Deprecating a single version of a package
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

When you deprecate a version fo a package, a red message will be displayed on that version’s package page, similar to deprecating an entire package.

.. figure:: https://docs.npmjs.com/assets/images/packages-and-modules/deprecate-version.png
   :alt: deprecation message saying version no longer supported upgrade to @latest

To deprecate a package version, run the following command, replacing **<package-name>** with the name of your package, **<version>** with your version number, and "**<message>**" with your deprecation message::

    npm deprecate <package-name>@<version> "<message>"

The CLI will also accept version ranges for **<version>**.

If you have two-factor auth, add a one-time password to the command, **--otp=123456** (where *123456* is the code from your authenticator).

Undeprecating a package or version
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To undeprecate a package, replace "**<message>**" with "" (an empty string) in one of the above commands.

For example, to undeprecate a package version, run the following command, replacing <package-name> with the name of your package, and <version> with your version number::

    npm deprecate <package-name>@<version> ""

If you have two-factor auth, add a one-time password to the command, **--otp=123456** (where *123456* is the code from your authenticator).

Transferring a deprecated package to npm
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you are no longer maintaining a package, but other users depend on it, and you’d like to remove it from your user profile, you can transfer it to the **@npm** user account, which is owned by npm, Inc.

.. note:: Once you transfer a package to the npm account, you will no longer be able to update it.

To transfer a package to the npm user account, run the following two commands in order, replacing <user> with your npm user name, and <package-name> with the package you want to transfer::

  npm owner add npm <package-name>
  npm owner rm <user> <package-name>

If you have two-factor auth, add a one-time password to the command, **--otp=123456** (where *123456* is the code from your authenticator).
