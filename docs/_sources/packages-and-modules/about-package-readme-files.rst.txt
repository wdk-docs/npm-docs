About package README files
===============================

To help others find your packages on npm and have a good experience using your code in their projects, we recommend including a README file in your package directory. Your README file may include directions for installing, configuring, and using the code in your package, as well as any other information a user may find helpful. The README file will be shown on the package page.

An npm package README file must be in the root-level directory of the package.

Creating and adding a README.md file to a package
--------------------------------------------------------------------------

In a text editor, in your package root directory, create a file called README.md.
In the README.md file, add useful information about your package.
Save the README.md file.
Note: The file extension .md indicates a Markdown file. For more information about Markdown, see the GitHub Guide "Mastering Markdown".

Updating an existing package README file
--------------------------------------------------------------------------
The README file will only be updated on the package page when you publish a new version of your package. To update your README file:

In a text editor, update the contents of the README.md file.
Save the README.md file.
On the command line, in the package root directory, run the following commands:
  npm version patch
  npm publish
