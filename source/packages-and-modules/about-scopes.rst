About scopes
========================

.. note::
   You must be using npm version 2 or greater to use scopes.
   To upgrade to the latest version of npm, on the command line, run **npm install npm@latest -g**

When you sign up for an npm user account or create an Org, you are granted a scope that matches your user or Org name. You can use this scope as a namespace for related packages.

A scope allows you to create a package with the same name as a package created by another user or Org without conflict.

When listed as a dependent in a package.json file, scoped packages are preceded by their scope name. The scope name is everything between the @ and the slash:

- **“npm” scope**::

    @npm/package-name

- **“npmcorp” scope**::

    @npmcorp/package-name

To create and publish public scoped packages, see :doc:`creating-and-publishing-scoped-public-packages`.

To create and publish private scoped packages, see :doc:`creating-and-publishing-private-packages`.

Scopes and package visibility
-------------------------------------------------------

- Unscoped packages are always public.
- :doc:`about-private-packages` are always scoped.
- Scoped packages are private by default; you must pass a command-line flag when publishing to make them public.

For more information on package scope and visibility, see :doc:`package-scope-access-level-and-visibility`.
