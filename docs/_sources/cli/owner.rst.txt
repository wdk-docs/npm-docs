npm owner
============================================================================================


SYNOPSIS
-------------------

.. program:: npm

.. option:: owner

   Manage package owners

   .. code-block:: sh

      npm owner add <user> [<@scope>/]<pkg>
      npm owner rm <user> [<@scope>/]<pkg>
      npm owner ls [<@scope>/]<pkg>

.. option:: author

   owner alias

DESCRIPTION
-------------------

Manage ownership of published packages.

ls: List all the users who have access to modify a package and push new versions. Handy when you need to know who to bug for help.
add: Add a new user as a maintainer of a package. This user is enabled to modify metadata, publish new versions, and add other owners.
rm: Remove a user from the package owner list. This immediately revokes their privileges.
Note that there is only one level of access. Either you can modify a package, or you can’t. Future versions may contain more fine-grained access levels, but that is not implemented at this time.

If you have two-factor authentication enabled with auth-and-writes then you’ll need to include an otp on the command line when changing ownership with --otp.

SEE ALSO
-------------------

- :option:`npm publish`
- :ref:`registry`
- :option:`npm adduser`
- :option:`npm disputes`
