npm uninstall
============================================================================================

SYNOPSIS
-------------------

.. program:: npm

.. option:: uninstall

   Remove a package

   .. code-block:: sh

      npm uninstall [<@scope>/]<pkg>[@<version>]... [-S|--save|-D|--save-dev|-O|--save-optional|--no-save]

.. option:: remove

   uninstall alias

.. option:: rm

   uninstall alias

.. option:: r

   uninstall alias

.. option:: un

   uninstall alias

.. option:: unlink

   uninstall alias

DESCRIPTION
-------------------

This uninstalls a package, completely removing everything npm installed on its behalf.

Example:

npm uninstall sax
In global mode (ie, with -g or --global appended to the command), it uninstalls the current package context as a global package.

npm uninstall takes 3 exclusive, optional flags which save or update the package version in your main package.json:

-S, --save: Package will be removed from your dependencies.

-D, --save-dev: Package will be removed from your devDependencies.

-O, --save-optional: Package will be removed from your optionalDependencies.

--no-save: Package will not be removed from your package.json file.

Further, if you have an npm-shrinkwrap.json then it will be updated as well.

Scope is optional and follows the usual rules for npm-scope.

Examples:

npm uninstall sax --save
npm uninstall @myorg/privatepackage --save
npm uninstall node-tap --save-dev
npm uninstall dtrace-provider --save-optional
npm uninstall lodash --no-save

SEE ALSO
-------------------

- :option:`npm prune`
- :option:`npm install`
- :ref:`folders`
- :option:`npm config`
- :option:`npm config`
- :ref:`npmrc`
