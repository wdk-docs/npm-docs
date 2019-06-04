Revoking authentication tokens
==================================================================

To keep your account and packages secure, we strongly recommend revoking (deleting) tokens you no longer need or that have been compromised. You can revoke any token you have created.

Note: While authentication tokens are not derived from your password, changing your password will invalidate all of your tokens. You can also invalidate a single token by logging out on a machine that is logged in with that token. We recommend revoking rather than invalidating tokens.
To see a list of your tokens, on the command line, run:
npm token list
In the tokens table, find and copy the ID of the token you want to delete.
On the command line, run the following command, replacing 123456 with the ID of the token you want to delete:
npm token delete 123456
npm will report Removed 1 token

To confirm that the token has been removed, run:
npm token list
Note: You must use the token ID to delete a token, not the truncated version of the token. In some cases, there may be a delay of up to an hour before a token is successfully revoked.
