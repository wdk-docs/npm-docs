Using npm packages in your projects
===========================================================================================

Once you have :doc:`downloading-and-installing-packages` in node_modules, you can use it in your code.

Using unscoped packages in your projects
-------------------------------------------------------

Node.js module
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you are creating a Node.js module, you can use a package in your module by passing it as an argument to the **require** function.

Example: using lodash in a Node.js module
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

For example, to use the lodash package in a Node.js module, in the root directory of the module, create a file named **index.js** with the following contents:

.. code-block:: js

  // index.js
  var lodash = require('lodash');

  var output = lodash.without([1, 2, 3], 1);
  console.log(output);

Run the code using **node index.js**. It should output [2, 3].

package.json file
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In **package.json**, list the package under dependencies. You can optionally include a semantic version.

.. code-block:: json

    {
      "dependencies": {
        "@package_name": "^1.0.0"
      }
    }

Using scoped packages in your projects
-------------------------------------------------------

To use a scoped package, simply include the scope wherever you use the package name.

Node.js module
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

When requiring a scoped package in the index.js file of your Node.js module,
you must reference the scope in addition to the package name:

.. code-block:: js

   var projectName = require("@scope/package-name")

package.json file
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In **package.json**:

.. code-block:: json

  {
    "dependencies": {
      "@scope/package_name": "^1.0.0"
    }
  }

Resolving “Cannot find module” errors
-------------------------------------------------------

If you have not properly installed a package, you will receive an error when you try to use it in your code. For example, if you reference the **lodash** package without installing it, you would see the following error:

.. code-block::

  module.js:340
      throw err;
            ^

  Error: Cannot find module 'lodash'

To resolve “cannot find module” errors, run the appropriate **install** command in the same directory as your project’s **index.js** file:

- For scoped packages, run ``npm install <@scope/package_name>``
- For unscoped packages, run ``npm install <package_name>``
