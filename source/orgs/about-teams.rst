About teams
====================================================================

Teams are groups of Org members with defined access to a set of packages governed by the Org.

The Developers team§
The Developers team is automatically created when you create an Org. By default, the Developers team has read/write access to all new packages created under the Org’s scope.

Members added to the Org, including the Org owner, are automatically added to the Developers team
The maintainers field in the package.json of any newly created packages under the Org scope is automatically populated with the members of the current Developers team
If you create a new package under your Org’s scope and you do not want members of the Developers team to have read/write access to that package, an owner or admin can remove the Developers team’s access to that package. For more informations, see “Managing team access to Org packages”.

If an owner adds a new member to an Org and does not want that member to be on the Developers team, an owner can remove them.

Removing the Developers team§
.. note:: We strongly recommend not removing the Developers team.

If an Org owner or admin deletes the Developers team:

Newly added members of the Org will not be added to any team.
Package access that current members had because they were a member of the Developers team will be removed.
npm will attempt to fill the maintainers field in package.json of newly created packages under the Org scope with the members of a team the publishing user belongs to. This behavior is not predictable.
Recreating the Developers team§
An Org owner or team admin can recreate the Developers team by creating a new team named “Developers”. The new Developers team will have all the default behavior of the original Developers team. An Org owner or admin will need to add members of the original Developers team to the new Developers team.
