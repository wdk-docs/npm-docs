npm ls
============================================================================================


SYNOPSIS
-------------------

.. program:: npm

.. option:: ls [[<@scope>/]<pkg> ...]

   List installed packages

.. option:: list

   ls alias

.. option:: la

   ls alias

.. option:: ll

   ls alias

DESCRIPTION
-------------------

This command will print to stdout all the versions of packages that are installed, as well as their dependencies, in a tree-structure.

Positional arguments are name@version-range identifiers,
which will limit the results to only the paths to the packages named.
Note that nested packages will also show the paths to the specified packages.
For example, running npm ls promzard in npm’s source tree will show::

  npm@@VERSION@ /path/to/npm
  └─┬ init-package-json@0.0.4
    └── promzard@0.1.5

It will print out extraneous, missing, and invalid packages.

If a project specifies git urls for dependencies these are shown in parentheses after the name@version to make it easier for users to recognize potential forks of a project.

The tree shown is the logical dependency tree, based on package dependencies, not the physical layout of your node_modules folder.

When run as ll or la, it shows extended information by default.

CONFIGURATION
-------------------

.. option:: ls --json <Boolean>

   Show information in JSON format.

   :Default: false
   :Type: Boolean


.. option:: ls --long <Boolean>

   Show extended information.

   :Default: false
   :Type: Boolean


.. option:: ls --parseable <Boolean>

   Show parseable output instead of tree view.

   :Default: false
   :Type: Boolean


.. option:: ls --global <Boolean>

   List packages in the global install prefix instead of in the current project.

   :Default: false
   :Type: Boolean

.. option:: ls --depth <int>

   Max display depth of the dependency tree.

   :Type: Int

.. option:: ls --prod/production <Boolean>

   Display only the dependency tree for packages in dependencies.

   :Type: Boolean
   :Default: false

.. option:: ls --dev/development <Boolean>

   Display only the dependency tree for packages in devDependencies.

   :Type: Boolean
   :Default: false

.. option:: ls --only <String>

   When “dev” or “development”, is an alias to dev.

   When “prod” or “production”, is an alias to production.

   :Type: String


.. option:: ls --link <Boolean>

   Display only dependencies which are linked

   :Type: Boolean
   :Default: false

SEE ALSO
-------------------

- :option:`npm config`
- :option:`npm config`
- :ref:`npmrc`
- :ref:`folders`
- :option:`npm install`
- :option:`npm link`
- :option:`npm prune`
- :option:`npm outdated`
- :option:`npm update`
