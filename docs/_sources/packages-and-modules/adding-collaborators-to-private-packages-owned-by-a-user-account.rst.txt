Adding collaborators to private packages owned by a user account
===========================================================================================

As an npm user with a paid user account, you can another npm user with a paid account as a collaborator on a private package you own.

Note: The user you want to add as a collaborator on your private package must have a paid user account. To sign up for a paid account, they can visit https://https://www.npmjs.com/settings/username/billing, replacing username with their npm username.

Granting access to a private user package on the web
-------------------------------------------------------

On the npm website, go to the package to which you want to add a collaborator: https://www.npmjs.com/package/<your-package-name>
On the package page, under “Collaborators”, click +.
Enter the npm username of the collaborator.
Click Submit.

Granting private package access from the command line interface
-------------------------------------------------------

To add a collaborator to a package on the command line, run the following command, replacing <user> with the npm username of your collaborator, and <your-package-name> with the name of the private package:

npm owner add <user> <your-package-name>

Granting access to private Org packages
-------------------------------------------------------

To grant an npm user access to private Org packages, you must have an Org owner add them to your Org, then add them to a team that has access to the private package. For more information, see “Adding members to your Org”.
