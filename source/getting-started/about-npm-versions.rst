About npm CLI versions
===============================================================================

The npm command line interface (CLI) is released on a regular cadence. We recommend installing the release that supports your workflow:

latest release: the most recent stable version.
next release: the most recent unreleased version of npm that is eventually released as the latest version.
The latest release of npm
The latest release of npm is the most recent stable version. When you install Node.js, npm is automatically installed. However, npm is released more frequently than Node.js, so to install the latest stable version of npm, on the command line, run:

npm install npm@latest -g
The next release of npm
Note: The next release of npm may contain features that do not match the features ultimately released in the latest stable version of npm.
The next release of npm is the most recent unreleased version of npm that is eventually released as the latest version. You may want to update your npm client to the next release to test your packages against it before latest is released.

To update to the next release of npm, on the command line, run:

npm install npm@next -g
Note: Depending on the development cycle, npm install npm@next -g may reinstall the latest release of npm.
