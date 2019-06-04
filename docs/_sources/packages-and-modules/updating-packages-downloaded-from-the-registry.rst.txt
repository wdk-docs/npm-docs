Updating packages downloaded from the registry
===========================================================================================

Updating local and global packages you downloaded from the registry helps keep your code and tools stable, usable, and secure.

Updating local packages
-------------------------------------------------------

We recommend regularly updating the local packages your project depends on to improve your code as improvements to its dependencies are made.

Navigate to the root directory of your project and ensure it contains a package.json file:
cd /path/to/project
In your project root directory, run the update command:
npm update
To test the update, run the outdated command. There should not be any output.
npm outdated

Updating globally-installed packages
-------------------------------------------------------

Note: If you are using npm version 2.6.0 or less, run this script to update all outdated global packages. However, please consider upgrading to the latest version of npm: npm install npm@latest -g

Determining which global packages need updating
-------------------------------------------------------

To see which global packages need to be updated, on the command line, run:

npm outdated -g --depth=0

Updating a single global package
-------------------------------------------------------

To update a single global package, on the command line, run:

npm update -g <package_name>

Updating all globally-installed packages
-------------------------------------------------------

To update all global packages, on the command line, run:

npm update -g

Resources
-------------------------------------------------------


CLI commands
-------------------------------------------------------

npm-update
npm-outdated
