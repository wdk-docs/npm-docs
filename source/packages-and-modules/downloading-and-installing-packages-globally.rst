Downloading and installing packages globally
===========================================================================================

.. tip:: If you are using npm 5.2 or higher, we recommend using npx to run packages globally.

Installing a package globally allows you to use the code in the package as a set of tools on your local computer.

To download and install packages globally, on the command line, run the following command::

    npm install -g <package_name>

If you get an EACCES permissions error,
you may need to reinstall npm with a version manager or manually change npm’s default directory.
For more information, see “Resolving EACCES permissions errors when installing packages globally”.
