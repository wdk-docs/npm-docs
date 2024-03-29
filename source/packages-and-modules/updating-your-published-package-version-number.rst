Updating your published package version number
==================================================

When you make significant changes to a published package, we recommend updating the version number to communicate the extent of the changes to others who rely on your code.

.. note:: If you have linked a git repository to a package, updating the package version number will also add a tag with the updated release number to the linked git repository.

1. To change the version number in package.json, on the command line, in the package root directory, run the following command, replacing <update_type> with one of the semantic versioning release types (patch, major, or minor)::

    npm version <update_type>

2. Run npm publish.
3. Go to your package page (https://npmjs.com/package/<package>) to check that the package version has been updated.

For more information on :option:`npm version`, see the CLI documentation.
