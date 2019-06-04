npm-config
============================================================================================

SYNOPSIS
-------------------
.. program:: npm

.. option:: config

   Manage the npm configuration files

   .. code-block::

      npm config set <key> <value> [-g|--global]
      npm config get <key>
      npm config delete <key>
      npm config list [-l] [--json]
      npm config edit
      npm get <key>
      npm set <key> <value> [-g|--global]

      aliases: c

DESCRIPTION
-------------------

npm gets its config settings from the command line, environment variables, :doc:`../files/npmrc` files, and in some cases, the :doc:`../files/package.json` file.

See :doc:`../files/npmrc` for more information about the npmrc files.

See :option:`npm config` for a more thorough discussion of the mechanisms involved.

The :option:`npm config` command can be used to update and edit the contents of the user and global npmrc files.

Sub-commands
-------------------

Config supports the following sub-commands:

set
~~~~~~~~~~~~~~

npm config set key value
Sets the config key to the value.

If value is omitted, then it sets it to “true”.

get
~~~~~~~~~~~~~~

.. code-block::

   npm config get key

Echo the config value to stdout.

list
~~~~~~~~~~~~~~

.. code-block::

   npm config list

Show all the config settings. Use -l to also show defaults. Use --json to show the settings in json format.

delete
~~~~~~~~~~~~~~

.. code-block::

   npm config delete key

Deletes the key from all configuration files.

edit
~~~~~~~~~~~~~~

.. code-block::

   npm config edit

Opens the config file in an editor. Use the --global flag to edit the global config.

SEE ALSO
-------------------

- :ref:`folders`
- :option:`npm config`
- :ref:`package.json`
- :ref:`npmrc`
- :option:`npm`
