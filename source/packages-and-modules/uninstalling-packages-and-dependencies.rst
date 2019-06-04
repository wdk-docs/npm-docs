Uninstalling packages and dependencies
===========================================================================================

If you no longer need to use a package in your code, we recommend uninstalling it and removing it from your project’s dependencies.

Uninstalling local packages
-------------------------------------------------------

Removing a local package from your node_modules directory
-------------------------------------------------------

To remove a package from your node_modules directory, on the command line, use the uninstall command. Include the scope if the package is scoped.

Unscoped package
-------------------------------------------------------

npm uninstall <package_name>

Scoped package
-------------------------------------------------------

npm uninstall <@scope/package_name>
Example
-------------------------------------------------------

npm uninstall lodash
Removing a local package from the package.json dependencies
-------------------------------------------------------

To remove a package from the dependencies in package.json, use the --save flag. Include the scope if the package is scoped.

Unscoped package
-------------------------------------------------------

npm uninstall --save <package_name>
Scoped package
-------------------------------------------------------

npm uninstall --save <@scope/package_name>

Example
-------------------------------------------------------

npm uninstall --save lodash
Note: If you installed a package as a "devDependency" (i.e. with --save-dev), use --save-dev to uninstall it: npm uninstall --save-dev package_name

Confirming local package uninstallation
-------------------------------------------------------

To confirm that npm uninstall worked correctly, check that the node_modules directory no longer contains a directory for the uninstalled package(s).

Unix system (such as OSX): ls node_modules
Windows systems: dir node_modules

Uninstalling global packages
-------------------------------------------------------

To uninstall an unscoped global package, on the command line, use the uninstall command with the -g flag. Include the scope if the package is scoped.

Unscoped package
-------------------------------------------------------

npm uninstall -g <package_name>

Scoped package
-------------------------------------------------------

npm uninstall -g <@scope/package_name>

Example
-------------------------------------------------------

For example, to uninstall a package called jshint, run:

npm uninstall -g jshint

Resources
-------------------------------------------------------

Uninstalling local packages
-------------------------------------------------------


Uninstalling global packages
-------------------------------------------------------

