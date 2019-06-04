audit to your continuous integration process.
===========================================================================================


command line audit report no vulnerabilities found

Turning off npm audit on package installation
-------------------------------------------------------

Installing a single package
-------------------------------------------------------

To turn off npm audit when installing a single package, use the --no-audit flag:

npm install example-package-name --no-audit

For more information, see the npm-install command.

Installing all packages
-------------------------------------------------------

To turn off npm audit when installing all packages, set the audit setting to false in your user and global npmrc config files:

npm set audit false

For more information, see the npm-config management command and the npm-config audit setting.
