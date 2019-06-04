About Org scopes and packages
=====================================================================================================

Every Org is granted an Org scope, a unique namespace for packages owned by the Org that matches the Org name. For example, an Org named “wombat” would have the scope @wombat.

You can use scopes to:

Maintain a fork of a package: @wombat/request.
Avoid name disputes with popular names: @wombat/web.
Easily find packages in the same namespace
Packages in a scope must follow the same naming guidelines as unscoped packages.

Managing unscoped packages§
While you are granted a scope by default when you create an Org, you can also use Orgs to manage unscoped packages, or packages under a different scope (such as a user scope).
