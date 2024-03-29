Adding dist-tags to packages
==================================

Distribution tags (dist-tags) are human-readable labels that you can use to organize and label different versions of packages you publish. dist-tags supplement :doc:`about-semantic-versioning`.
In addition to being more human-readable than semantic version numbering, tags allow publishers to distribute their packages more effectively.

For more information, see the :option:`npm dist-tag`.

.. note:: Since dist-tags share a namespace with semantic versions, avoid dist-tags that conflict with existing version numbers. We recommend avoiding dist-tags that start with a number or the letter "v".

Publishing a package with a dist-tag
-------------------------------------------------------

By default, running npm publish will tag your package with the latest dist-tag. To use another dist-tag, use the --tag flag when publishing.

1. On the command line, navigate to the root directory of your package.

  .. code-block:: sh

    cd /path/to/package

2. Run the following command, replacing <tag> with the tag you want to use:

  .. code-block:: sh

    npm publish --tag <tag>

**Example**

To publish a package with the “beta” dist-tag, on the command line, run the following command in the root directory of your package:

.. code-block:: sh

  npm publish --tag beta

Adding a dist-tag to a specific version of your package
-------------------------------------------------------

On the command line, navigate to the root directory of your package.

.. code-block:: sh

  cd /path/to/package

Run the following command, replacing <package_name> with the name of your package, <version> with your package version number, and <tag> with the distribution tag:

.. code-block:: sh

  npm dist-tag add <package-name>@<version> [<tag>]

**Example**

To add the “stable” tag to the 1.4.0 version of the “example-package” package, you would run the following command:

.. code-block:: sh

    npm dist-tag add example-package@1.4.0 stable
