About two-factor authentication
======================================

Two-factor authentication (2FA) protects against unauthorized access to your account by confirming your identity using:

- something you know (such as your username and password)
- something you have (such as a phone or tablet)

When you enable 2FA, we will prompt you for a unique one-time password when you perform certain actions on your account or on packages to which you have write access, depending on your 2FA configuration.

.. note:: Two-factor authentication provides the best possible security for your account against attackers. We strongly recommend enabling 2FA on your account as soon as possible after you sign up.

Two-factor authentication modes on npm
------------------------------------------------

Two-factor authentication on npm can be enabled for authorization only, or authorization and writes.

Authorization only
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you enable 2FA for authorization only, we will request a one-time password for certain authorized actions.

+---------------------------------------------------+----------------------------------+
|                      Action                       |           CLI command            |
+===================================================+==================================+
| Log in to npm                                     | npm login                        |
+---------------------------------------------------+----------------------------------+
| Change profile settings (including your password) | npm profile set                  |
+---------------------------------------------------+----------------------------------+
| Change 2FA modes for your user account            | npm profile enable-2fa auth-only |
+---------------------------------------------------+----------------------------------+
| Disable 2FA for your user account                 | npm profile disable-2fa          |
+---------------------------------------------------+----------------------------------+

Authorization and writes
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you enable 2FA for authorization and writes, we will request a one-time password for certain authorized actions, as well as write actions.

+---------------------------------------------------+----------------------------------+
|                      Action                       |           CLI command            |
+===================================================+==================================+
| Log in to npm                                     | npm login                        |
+---------------------------------------------------+----------------------------------+
| Change profile settings (including your password) | npm profile set                  |
+---------------------------------------------------+----------------------------------+
| Change 2FA modes for your user account            | npm profile enable-2fa auth-only |
+---------------------------------------------------+----------------------------------+
| Disable 2FA for your user account                 | npm profile disable-2fa          |
+---------------------------------------------------+----------------------------------+
| Create tokens                                     | npm token create                 |
+---------------------------------------------------+----------------------------------+
| Revoke tokens                                     | npm token revoke                 |
+---------------------------------------------------+----------------------------------+
| Publish packages                                  | npm publish                      |
+---------------------------------------------------+----------------------------------+
| Unpublish packages                                | npm unpublish                    |
+---------------------------------------------------+----------------------------------+
| Deprecate packages                                | npm deprecate                    |
+---------------------------------------------------+----------------------------------+
| Change package visibility                         | npm access public/restricted     |
+---------------------------------------------------+----------------------------------+
| Change user and team package access               | npm access grant/revoke          |
+---------------------------------------------------+----------------------------------+
| Change package 2FA requirements                   | N/A                              |
+---------------------------------------------------+----------------------------------+
