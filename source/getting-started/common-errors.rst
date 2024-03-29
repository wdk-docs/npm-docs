Common errors
===============================================================================

Errors
------------------------------------------------

- Broken npm installation
- Random errors
- No compatible version found
- Permissions errors
- Error: ENOENT, stat 'C:\Users\<user>\AppData\Roaming\npm' on Windows 7
- No space
- No git
- Running a Vagrant box on Windows fails due to path length issues
- npm only uses git: and ssh+git: URLs for GitHub repos, breaking proxies
- SSL error
- SSL-intercepting proxy
- Not found / Server error
- Invalid JSON
- Many ENOENT / ENOTEMPTY errors in output
- cb() never called! when using shrinkwrapped dependencies
- npm login errors
- npm hangs on Windows at addRemoteTarball
- npm not running the latest version on a Windows machine

Broken npm installation
------------------------------------------------

If your npm is broken:

- On Mac or Linux, reinstall npm.
- Windows: If you’re on Windows and you have a broken installation, the easiest thing to do is to reinstall node from the official installer (see this note about installing the latest stable version).

Random errors
------------------------------------------------

- Some strange issues can be resolved by simply running npm cache clean and trying again.
- If you are having trouble with npm install, use the -verbose option to see more details.

No compatible version found
------------------------------------------------

You have an outdated npm. Please update to the latest stable npm.

Permissions errors
------------------------------------------------

Please see the discussions in “Downloading and installing Node.js and npm” and “Resolving EACCES permissions errors when installing packages globally” for ways to avoid and resolve permissions errors.

Error: ENOENT, stat 'C:\Users\<user>\AppData\Roaming\npm' on Windows 7
----------------------------------------------------------------------------------------

The error Error: ENOENT, stat 'C:\Users\<user>\AppData\Roaming\npm' on Windows 7 is a consequence of joyent/node#8141, and is an issue with the Node installer for Windows. The workaround is to ensure that C:\Users\<user>\AppData\Roaming\npm exists and is writable with your normal user account.

No space
----------------------------------------------------------------------------------------

.. code-block:: sh

    npm ERR! Error: ENOSPC, write

You are trying to install on a drive that either has no space, or has no permission to write.

- Free some disk space or
- Set the tmp folder somewhere with more space: npm config set tmp /path/to/big/drive/tmp or
- Build Node yourself and install it somewhere writable with lots of space.

No git
----------------------------------------------------------------------------------------

.. code-block:: sh

    npm ERR! not found: git
    ENOGIT

You need to install git. Or, you may need to add your git information to your npm profile. You can do this from the command line or the website. For more information, see “Managing your profile settings”.

Running a Vagrant box on Windows fails due to path length issues
----------------------------------------------------------------------------------------

@drmyersii went through what sounds like a lot of painful trial and error to come up with a working solution involving Windows long paths and some custom Vagrant configuration::

   This is the commit that I implemented it in, but I’ll go ahead and post the main snippet of code here::

    config.vm.provider "virtualbox" do |v|
        v.customize ["sharedfolder", "add", :id, "--name", "www", "--hostpath", (("//?/" + File.dirname(__FILE__) + "/www").gsub("/","\\"))]
    end

    config.vm.provision :shell, inline: "mkdir /home/vagrant/www"
    config.vm.provision :shell, inline: "mount -t vboxsf -o uid=`id -u vagrant`,gid=`getent group vagrant | cut -d: -f3` > www /home/vagrant/www", run: "always"

   In the code above, I am appending \\?\ to the current directory absolute path. This will actually force the Windows API to allow an increase in the MAX_PATH variable (normally capped at 260). Read more about max path. This is happening during the sharedfolder creation which is intentionally handled by VBoxManage and not Vagrant’s “synced_folder” method. The last bit is pretty self-explanatory; we create the new shared folder and then make sure it’s mounted each time the machine is accessed or touched since Vagrant likes to reload its mounts/shared folders on each load.

npm only uses git: and ssh+git: URLs for GitHub repos, breaking proxies
----------------------------------------------------------------------------------------

@LaurentGoderre fixed this with some Git trickery:

I fixed this issue for several of my colleagues by running the following two commands::

.. code-block:: sh

    git config --global url."https://github.com/".insteadOf git@github.com:
    git config --global url."https://".insteadOf git://

One thing we noticed is that the .gitconfig used is not always the one expected so if you are on a machine that modified the home path to a shared drive, you need to ensure that your .gitconfig is the same on both your shared drive and in c:\users\[your user]\

SSL Error
----------------------------------------------------------------------------------------

npm ERR! Error: 7684:error:140770FC:SSL routines:SSL23_GET_SERVER_HELLO:unknown protocol:openssl\ssl\s23_clnt.c:787:
You are trying to talk SSL to an unencrypted endpoint. More often than not, this is due to a proxy configuration error (see also this helpful, if dated, guide). In this case, you do not want to disable strict-ssl – you may need to set up a CA / CA file for use with your proxy, but it’s much better to take the time to figure that out than disabling SSL protection.

.. code-block:: sh

    npm ERR! Error: SSL Error: CERT_UNTRUSTED
    npm ERR! Error: SSL Error: UNABLE_TO_VERIFY_LEAF_SIGNATURE

This problem will happen if you’re running Node 0.6. Please upgrade to node 0.8 or above. See this post for details.

You could also try these workarounds: npm config set ca "" or npm config set strict-ssl false

.. code-block:: sh

    npm ERR! Error: SSL Error: SELF_SIGNED_CERT_IN_CHAIN
    npm no longer supports its self-signed certificates

Either:

upgrade your version of npm npm install npm -g --ca=""
tell your current version of npm to use known registrars npm config set ca=""
If this does not fix the problem, then you may have an SSL-intercepting proxy. (For example, https://github.com/npm/npm/issues/7439#issuecomment-76024878)

SSL-intercepting proxy
----------------------------------------------------------------------------------------

Unsolved. See https://github.com/npm/npm/issues/9282

Not found / Server error
----------------------------------------------------------------------------------------

.. code-block::

    npm http 404 https://registry.npmjs.org/faye-websocket/-/faye-websocket-0.7.0.tgz
    npm ERR! fetch failed https://registry.npmjs.org/faye-websocket/-/faye-websocket-0.7.0.tgz
    npm ERR! Error: 404 Not Found
    npm http 500 https://registry.npmjs.org/phonegap

It’s most likely a temporary npm registry glitch. Check npm server status and try again later.
If the error persists, perhaps the published package is corrupt. Contact the package owner and have them publish a new version of the package.

Invalid JSON
----------------------------------------------------------------------------------------

.. code-block:: sh

    Error: Invalid JSON
    npm ERR! SyntaxError: Unexpected token <
    npm ERR! registry error parsing json

Possible temporary npm registry glitch, or corrupted local server cache. Run npm cache clean and/or try again later.
This can be caused by corporate proxies that give HTML responses to package.json requests. Check npm’s proxy configuration.
Check that it’s not a problem with a package you’re trying to install (e.g. invalid package.json).

Many ENOENT / ENOTEMPTY errors in output
----------------------------------------------------------------------------------------

npm is written to use resources efficiently on install, and part of this is that it tries to do as many things concurrently as is practical. Sometimes this results in race conditions and other synchronization issues. As of npm 2.0.0, a very large number of these issues were addressed. If you see ENOENT lstat, ENOENT chmod, ENOTEMPTY unlink, or something similar in your log output, try updating npm to the latest version. If the problem persists, look at npm/npm#6043 and see if somebody has already discussed your issue.

cb() never called! when using shrinkwrapped dependencies
----------------------------------------------------------------------------------------

Take a look at issue #5920. We’re working on fixing this one, but it’s a fairly subtle race condition and it’s taking us a little time. You might try moving your npm-shrinkwrap.json file out of the way until we have this fixed. This has been fixed in versions of npm newer than npm@2.1.5, so update to npm@latest.

npm login errors
----------------------------------------------------------------------------------------

Sometimes npm login fails for no obvious reason. The first thing to do is to log in at https://www.npmjs.com/login and check that your e-mail address on npmjs.com matches the email address you are giving to npm login.

If that’s not the problem, or if you are seeing the message "may not mix password_sha and pbkdf2", then

1. Log in at https://npmjs.com/
2. Change password at https://npmjs.com/password – you can even “change” it to the same password
3. Clear login-related fields from ~/.npmrc – e.g., by running sed -ie '/registry.npmjs.org/d' ~/.npmrc
4. npm login

and it generally seems to work.

See https://github.com/npm/npm/issues/6641#issuecomment-72984009 for the history of this issue.

npm hangs on Windows at addRemoteTarball
----------------------------------------------------------------------------------------

Check if you have two temp directories set in your .npmrc:


.. code-block:: sh

    > npm config ls -l

Look for lines defining the tmp config variable. If you find more than one, remove all but one of them.

See https://github.com/npm/npm/issues/7590 for more about this unusual problem.

npm not running the latest version on a Windows machine
----------------------------------------------------------------------------------------

See the section about Windows here.
