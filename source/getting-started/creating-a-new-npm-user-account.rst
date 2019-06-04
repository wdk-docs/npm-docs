Creating a new user account on the public registry
===========================================================

If you do not already have an npm user account, you can create an account in order to share and download Javascript packages on the public registry.

.. note:: If you are using an npm Enterprise registry, you must log in with your SSO credentials instead of creating an account. For more information, contact your company's Enterprise admin.

Creating an account on the website
-----------------------------------------

1. Go to the npm signup page.
2. In the user signup form, type in the fields:

   - Full name
   - Public email: Your public email address will be added to the metadata of your packages and will be visible to anyone who downloads your packages. We will also send email to this account when you update packages, as well as occasional product updates and information.
   - Username: The username that will be displayed when you publish packages or interact with other npm users on npmjs.com. Your username must be lower case, and can contain hyphens and numerals.
   - Password: Your password must meet our password guidelines. new account signup form

3. To sign up for our email newsletter, select “Sign up for the npm Weekly”. sign up for the npm weekly checkbox selected
4. Select “Agree to the End User License Agreement and the Privacy Policy”. agree to the end user license agreement and privacy policy checkbox selected
5. Click Create An Account. create an account button

.. note:: After signing up for an npm account, you will receive an account verification email. You must verify your email address in order to publish packages to the registry.
Testing your new account with npm login

Use the npm login command to test logging in to your new account.
-------------------------------------------------------------------------------

.. note:: If you misspell your existing account username when you log in with the npm login command, you will create a new account with the misspelled name. For help with accidentally-created accounts, contact npm Support.

1. On the command line, type the following command, replacing

   .. code-block:: sh

      npm login

2. When prompted, enter your username, password, and email address.
3. If you have two-factor authentication enabled, when prompted, enter a one-time password.
4. To test that you have successfully logged in, type:

   .. code-block::

      npm whoami

   Your npm username should be displayed.
