Renaming an Org
=====================================================================================================

Orgs cannot be renamed from the website or command line interface.

To rename an Org, as an Org owner, you must manually migrate your existing Org members, teams, and packages to a new Org, then contact npm Support to have the outdated packages unpublished and the previous Org deleted.

Create a new Org with the name you want. If your old Org is on a paid plan, you must choose a paid plan for the new Org.
Add the members of your old Org to your new Org.
In your new Org, create teams to match teams in your old Org.
Republish packages to the new Org by updating the package scope in its package.json file to match the new Organization name and running npm publish.
In the new Org teams, configure package access to match team package access in your old Org.
Contact npm Support to have the outdated packages unpublished and the previous Org deleted.
