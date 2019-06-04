Unpublishing packages from the registry
===========================================================================================

In order to permanently remove a package (or package version) from the npm registry, as a package owner or collaborator, you can unpublish it from the the command line within 72 hours of the initial publish.

If you want to unpublish a package after 72 hours have passed, contact npm Support. For more information about why we don’t allow users to unpublish packages after 72 hours, see our unpublish policy.

Note: If you are using npm Enterprise, you can have an admin contact npm Enterprise Support at enterprise@npmjs.com to increase the unpublishing window for your instance beyond 72 hours.
Unpublishing a package using the CLI or by contacting npm support is the only way to remove a package or version from the registry. For example, removing all the collaborators or teams from the package will not unpublish it.

If you are no longer interested in maintaining a package, but want it to remain available for users to install, or if your package has dependents, we’d recommend deprecating it. To learn about how to deprecate a package, see “Deprecating and undeprecating packages or package versions”.

Unpublishing a package permanently removes the package from the registry so it is no longer available for other users to install. Once a package is unpublished, it cannot be republished. If you’ve unpublished a package by mistake, we’d recommend publishing again under a different name, or for unpublished versions, bumping the version number and publishing again.

You might want to unpublish a package because you:

Published something accidentally.
Wanted to test npm.
Published content you didn’t intend to be public.
Wanted to rename a package. (The only way to rename a package is to re-publish it under a new name)
Note: Since various systems rely on package-name@version being unique, you cannot reuse a published version by unpublishing and re-publishing it. If you want to reuse a version number, we recommend publishing a minor version update instead.

Unpublishing an entire package
-------------------------------------------------------

To unpublish an entire package, run the following command, replacing <package-name> with the name of your package:

npm unpublish <package-name> -f
If you have two-factor authentication enabled for writes, you will need to add a one-time password to the unpublish command, --otp=123456 (where 123456 is the code from your authenticator app).

Unpublishing a single version of a package
-------------------------------------------------------

To unpublish a single version of a package, run the following command, replacing <package-name> with the name of your package, and <version> with your version number:

npm unpublish <package-name>@<version>
If you have two-factor auth, add a one-time password to the command, --otp=123456 (where 123456 is the code from your authenticator).
