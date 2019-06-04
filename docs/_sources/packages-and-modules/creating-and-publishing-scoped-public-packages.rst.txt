Creating and publishing scoped public packages
===================================================

To share your code publicly in a user or Org namespace, you can publish public user-scoped or Org-scoped packages to the npm registry.

For more information on scopes, see “About scopes”.

Note: Before you can publish user-scoped npm packages, you must sign up for an npm user account. Additionally, to publish Org-scoped packages, you must create an npm user account, then create an npm Org.

Overview
-------------------------------------------------------

Create your package
Review package contents for sensitive or unnecessary information
Publish your package

Creating a scoped public package
-------------------------------------------------------

If you are using npmrc to manage accounts on multiple registries, on the command line, switch to the appropriate profile:
 npmrc <profile-name>
On the command line, create a directory for your package:
 mkdir my-test-package
Navigate to the root directory of your package:
 cd my-test-package
If you are using git to manage your package code, in the package root directory, run the following commands, replacing git-remote-url with the git remote URL for your package:
 git init
 git remote add origin git://git-remote-url
In the package root directory, run the npm init command and pass the scope to the scope flag:
For an Org-scoped package, replace my-org with the name of your Org:
 npm init --scope=@my-org
For a user-scoped package, replace my-username with your username:
 npm init --scope=@my-username
Respond to the prompts to generate a package.json file. For help naming your package, see “Package name guidelines”.
Create a README file that explains what your package code is and how to use it.
In your preferred text editor, write the code for your package.

Reviewing package contents for sensitive or unnecessary information
-------------------------------------------------------

Publishing sensitive information to the registry can harm your users, compromise your development infrastructure, be expensive to fix, and put you at risk of legal action. We strongly recommend removing sensitive information, such as private keys, passwords, personally identifiable information (PII), and credit card data before publishing your package to the registry.

For less sensitive information, such as testing data, use a .npmignore or .gitignore file to prevent publishing to the registry. For more information, see this article.

Publishing scoped public packages
-------------------------------------------------------

By default, scoped packages are published with private visibility. To publish a scoped package with public visibility, use npm publish --access public.

On the command line, navigate to the root directory of your package.
 cd /path/to/package
To publish your scoped public package to the npm registry, run:
 npm publish --access public
To see your public package page, visit https://npmjs.com/package/package-name, replacing package-name with the name of your package. Public packages will say public below the package name on the npm website.
public package page showing public below package name

For more information on the publish command, see the CLI documentation.

< Creating and publishing unscoped public packages | Creating and publishing private packages >
