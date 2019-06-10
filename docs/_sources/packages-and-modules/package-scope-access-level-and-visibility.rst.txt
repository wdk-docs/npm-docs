npm package scope, access level, and visibility
====================================================

Visibility of npm packages depends on the scope (namespace) in which the package is contained, and the access level (private or public) set for the package.

.. note::
   To create Org-scoped packages, you must first create an Org. For more information, see :doc:`../orgs/creating-an-org`.

Public registry
---------------------------------------------

+----------+--------------+------------------------------------------------------------------------------+----------------------------------------------------------------------------------------+
|  Scope   | Access level |                            Can view and download                             |                                  Can write (publish)                                   |
+==========+==============+==============================================================================+========================================================================================+
| Org      | Private      | Members of a team in the Org with read access to the package                 | Members of a team in the Org with read and write access to the package                 |
+----------+--------------+------------------------------------------------------------------------------+----------------------------------------------------------------------------------------+
| Org      | Public       | Everyone                                                                     | Members of a team in the Org with read and write access to the package                 |
+----------+--------------+------------------------------------------------------------------------------+----------------------------------------------------------------------------------------+
| User     | Private      | The package owner and users who have been granted read access to the package | The package owner and users who have been granted read and write access to the package |
+----------+--------------+------------------------------------------------------------------------------+----------------------------------------------------------------------------------------+
| User     | Public       | Everyone                                                                     | The package owner and users who have been granted read and write access to the package |
+----------+--------------+------------------------------------------------------------------------------+----------------------------------------------------------------------------------------+
| Unscoped | Public       | Everyone                                                                     | The package owner and users who have been granted read and write access to the package |
+----------+--------------+------------------------------------------------------------------------------+----------------------------------------------------------------------------------------+

.. note:: Only user accounts can create and manage unscoped packages. Orgs can only manage scoped packages.

npm Enterprise
---------------------------------------------

The following table applies to customers who purchased npm Enterprise after July 26, 2018.

+----------+--------------+---------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------+
|  Scope   | Access level |                                                Can view and download                                                |                                                      Can write (publish)                                                      |
+==========+==============+=====================================================================================================================+===============================================================================================================================+
| Org      | Private      | Logged-in members of the Enterprise registry who belong to a team in the Org with read access to the package        | Logged-in members of the Enterprise registry who belong to a team in the Org with read and write access to the package        |
+----------+--------------+---------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------+
| Org      | Public       | All logged-in members of the Enterprise registry                                                                    | Logged-in members of the Enterprise registry who belong to a team in the Org with read and write access to the package        |
+----------+--------------+---------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------+
| User     | Private      | The package owner and logged-in members of the Enterprise registry who have been granted read access to the package | The package owner and logged-in members of the Enterprise registry who have been granted read and write access to the package |
+----------+--------------+---------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------+
| User     | Public       | All logged-in members of the Enterprise registry                                                                    | The package owner and logged-in members of the Enterprise registry who have been granted read and write access to the package |
+----------+--------------+---------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------+
| Unscoped | Public       | All users of the Enterprise registry                                                                                | None (see note below)                                                                                                         |
+----------+--------------+---------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------+

.. note:: The unscoped namespace on npm Enterprise is reserved for unscoped packages in the public npm registry. To prevent npm Enterprise users from accidentally publishing proprietary code to the public npm registry, where it would be visible to anyone on the internet, we do not allow publishing unscoped packages to npm Enterprise.

