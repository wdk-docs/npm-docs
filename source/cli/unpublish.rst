npm unpublish
============================================================================================


SYNOPSIS
-------------------

.. program:: npm

.. option:: unpublish

   Remove a package from the registry

   .. code-block:: sh

      npm unpublish [<@scope>/]<pkg>[@<version>]

WARNING
-------------------

It is generally considered bad behavior to remove versions of a library that others are depending on!

Consider using the deprecate command instead, if your intent is to encourage users to upgrade.

There is plenty of room on the registry.

DESCRIPTION
-------------------

This removes a package version from the registry, deleting its entry and removing the tarball.

If no version is specified, or if all versions are removed then the root package entry is removed from the registry entirely.

Even if a package version is unpublished, that specific name and version combination can never be reused. In order to publish the package again, a new version number must be used. Additionally, new versions of packages with every version unpublished may not be republished until 24 hours have passed.

With the default registry (registry.npmjs.org), unpublish is only allowed with versions published in the last 72 hours. If you are trying to unpublish a version published longer ago than that, contact support@npmjs.com.

The scope is optional and follows the usual rules for npm-scope.

SEE ALSO
-------------------

- :option:`npm deprecate`
- :option:`npm publish`
- :ref:`registry`
- :option:`npm adduser`
- :option:`npm owner`
