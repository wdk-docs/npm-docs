Recovering your 2FA-enabled account
============================================

Depending on the circumstances, you may be able to recover access to your 2FA-enabled account.

Misplaced second factor device
-------------------------------------

If you have misplaced the device that provided second-factor authentication, you can use the recovery codes generated when you enabled 2FA to access your account.

1. Locate the recovery codes generated when you enabled 2FA on your account.
2. If you are logged out, on the command line, log in using your npm username and npm password.

  .. code-block::

    npm login

3. When prompted for an OTP, enter a recovery code.
4. Once you are logged in, type npm profile disable-2fa and enter your npm password if prompted.
5. Enter an unused recovery code when you see this prompt:

  .. code-block::

    >Enter one-time password from your authenticator:

6. npm will confirm that two-factor authentication has been disabled.
7. type npm profile enable-2fa to re-enable 2FA, assign a different device to your account, and generate new recovery codes.

.. note:: Using the recovery codes to re-enable 2FA may create a second authenticator account with the same npm account name. To delete the old authenticator account, follow the steps for the authenticator.

Misplaced recovery codes
------------------------------

If you have misplaced both the device that provided second-factor authentication and your recovery codes, we may be unable to help you recover your account. If you have any questions, please `contact npm Support`_.

.. _contact npm Support: https://www.npmjs.com/support
