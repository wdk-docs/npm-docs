Configuring your npm client with your Org settings
=====================================================================================================

As an Org member, you can configure your npm client to:

make a single package or all new packages you create locally use your Org’s scope
make a single package or all new packages you create locally have default public visibility
Before configuring your npm client, you must install npm.

Configuring your npm client to use your Org’s scope§
If you will be publishing packages with your Org’s scope often, you can add your Org’s scope to your global .npmrc configuration file.

Setting your Org scope for all new packages§
.. note:: Setting the Org scope using the steps below will only set the scope for new packages; for existing packages, you will need to update the name field in package.json.

On the command line, type the following command:
 npm config set scope <org-name> --global
Press Enter.
For packages you do not want to publish with your Org’s scope, you must manually edit the package’s package.json to remove the Org scope from the name field.

Setting your Org scope for a single package§
On the command line, navigate to the package directory. cd /path/to/package
Type the following command, replacing with the name of your Org:
 npm config set scope <org-name>
Press Enter.
Changing default package visibility to public§
By default, publishing a scoped package with npm publish will publish the package as private. If you are a member of an Org on the free Org plan, or are on the paid Org plan but want to publish a scoped package as public, you must pass the --access public flag:

npm publish --access public.

Setting package visibility to public for a single package§
You can set a single package to pass --access public to every npm publish command that you issue for that package.

On the command line, navigate to the package directory. cd /path/to/package
Type the following command:
 npm config set access public
Press Enter.
Setting package visibility to public for all packages§
You can set all packages to pass --access public to every npm publish command that you issue for that package.

Warning: Setting packages access to public in your global .npmrc will affect all packages you create, including packages in your personal account scope, as well as packages scoped to your Org.

On the command line, type the following command:
 npm config set access public --global
Press Enter.
