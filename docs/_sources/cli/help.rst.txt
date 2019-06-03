npm-help
============================================================================================

Get help on npm

SYNOPSIS
-------------------

.. program:: npm

.. option:: help

npm help <term> [<terms..>]

DESCRIPTION
-------------------

If supplied a topic, then show the appropriate documentation page.

If the topic does not exist, or if multiple terms are provided, then run the help-search command to find a match. Note that, if help-search finds a single subject, then it will run help on that topic, so unique matches are equivalent to specifying a topic name.

CONFIGURATION
-------------------

viewer
Default: “man” on Posix, “browser” on Windows
Type: path
The program to use to view help content.

Set to "browser" to view html help content in the default web browser.

SEE ALSO
-------------------

- npm
- README
- npm-folders
- npm-config
- npm-config
- npmrc
- package.json
- npm-help-search
- npm-index
