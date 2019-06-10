npm completion
============================================================================================

SYNOPSIS
-------------------
.. program:: npm

.. option:: completion

   Tab Completion for npm

   .. code-block::

      source <(npm completion)

DESCRIPTION
-------------------

Enables tab-completion in all npm commands.

The synopsis above loads the completions into your current shell. Adding it to your **~/.bashrc** or **~/.zshrc** will make the completions available everywhere:

.. code-blcok::

   npm completion >> ~/.bashrc
   npm completion >> ~/.zshrc

You may of course also pipe the output of :option:`npm completion` to a file such as **/usr/local/etc/bash_completion.d/npm** or **/etc/bash_completion.d/npm** if you have a system that will read that file for you.

When **COMP_CWORD**, **COMP_LINE**, and **COMP_POINT** are defined in the environment, :option:`npm completion` acts in “plumbing mode”, and outputs completions based on the arguments.

SEE ALSO
-------------------

- :option:`npm developers`
- :program:`npm`
