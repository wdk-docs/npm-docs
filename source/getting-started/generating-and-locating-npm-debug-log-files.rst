Generating and locating npm-debug.log files
===============================================================================

When a package fails to install or publish, the npm CLI will generate an npm-debug.log file. This log file can help you (and npm Support) figure out what went wrong.

If you need to generate a npm-debug.log file, you can run one of these commands.

For installing packages:

.. code-block::

  npm install --timing

For publishing packages:

.. code-block::

  npm publish --timing

You can find the npm-debug.log file in your .npm directory. To find your .npm directory, use npm config get cache.

If you use a CI environment, your logs are likely located elsewhere. For example, in Travis CI, you can find them in the /home/travis/build directory.

.. note:: npm Enterprise users: If you need to contact npm Enterprise Support at enterprise@npmjs.com, we recommend attaching the entire contents of the npm-debug.log file or copying the contents into the body of the message, so that we can more easily diagnose the problem.
