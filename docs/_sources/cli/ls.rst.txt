npm-ls
============================================================================================


SYNOPSIS
-------------------

.. program:: npm

.. option:: ls

   List installed packages

   .. code-block:: sh

      npm ls [[<@scope>/]<pkg> ...]

   aliases: list, la, ll

DESCRIPTION
-------------------

This command will print to stdout all the versions of packages that are installed, as well as their dependencies, in a tree-structure.

Positional arguments are name@version-range identifiers, which will limit the results to only the paths to the packages named. Note that nested packages will also show the paths to the specified packages. For example, running npm ls promzard in npm’s source tree will show:

npm@@VERSION@ /path/to/npm
└─┬ init-package-json@0.0.4
  └── promzard@0.1.5
It will print out extraneous, missing, and invalid packages.

If a project specifies git urls for dependencies these are shown in parentheses after the name@version to make it easier for users to recognize potential forks of a project.

The tree shown is the logical dependency tree, based on package dependencies, not the physical layout of your node_modules folder.

When run as ll or la, it shows extended information by default.

CONFIGURATION
-------------------

json
Default: false
Type: Boolean
Show information in JSON format.

long
Default: false
Type: Boolean
Show extended information.

parseable
Default: false
Type: Boolean
Show parseable output instead of tree view.

global
Default: false
Type: Boolean
List packages in the global install prefix instead of in the current project.

depth
Type: Int
Max display depth of the dependency tree.

prod / production
Type: Boolean
Default: false
Display only the dependency tree for packages in dependencies.

dev / development
Type: Boolean
Default: false
Display only the dependency tree for packages in devDependencies.

only
Type: String
When “dev” or “development”, is an alias to dev.

When “prod” or “production”, is an alias to production.

link
Type: Boolean
Default: false
Display only dependencies which are linked

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
