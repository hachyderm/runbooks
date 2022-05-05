# Runbook: Account Approval

This runbook captures steps that should be followed when a new user applies for an account, and culminates in a decision to Approve or Reject.

## Steps

1. Navigate to the [pending accounts](https://hachyderm.io/admin/accounts?status=pending) page
2. Click on the pending account to review the application:
  * Read the "Reasons for joining" at the bottom of the page
  * Check the username and email to see if they give off a "bad" or "bot" vibe
    * A quick online search may help here.
3. If nothing worrisome is found, `Approve`. 
4. If something _might_ be off:
   1. Leave a moderation note on the account
   2. Post a notice to `hachyderm-mods` in chat to keep an eye on the user
   3. `Approve`
5. If the user is clearly a bad actor, `Reject`.
