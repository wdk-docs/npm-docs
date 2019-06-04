Creating and publishing an Org scoped package
=====================================================================================================

As an Org member, you can create and publish public and private packages within the Org’s scope.

Creating an Org scoped package§
On the command line, make a directory with the name of the package you would like to create.
   mkdir /path/to/package/directory
Navigate to the newly-created package directory.
To create an Org scoped package, on the command line, type:
   npm init --scope=<your_org_name>
Press Enter.
To verify the package is using your Org scope, in a text editor, open the package’s package.json file and check that the name is @your_org_name/<pkg_name>, replacing your_org_name with the name of your Org.
Publishing a private Org scoped package§
By default, npm publish will publish a scoped package as private.

By default, any scoped package is published as private. However, if you have an Org that does not have the Private Packages feature, npm publish will fail unless you pass the access flag.

On the command line, navigate to the package directory.
Type npm publish.
Press Enter.
Private packages will say private below the package name on the npm website.

private package page showing private below package name

Publishing a public Org scoped package§
To publish an Org scoped package as public, use npm publish --access public.

On the command line, navigate to the package directory.
Type npm publish --access public.
Press Enter.
Public packages will say public below the package name on the npm website.

public package page showing public below package name
