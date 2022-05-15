# Runbook: Server Blocking

This runbook captures steps that should be followed when a server block is suggested.

## Guiding Philosophy

We are committed to maintaining a safe space for our users and moderators. As such, treat all server-block suggestions with respect, and when faced with an ambiguous decision, default towards safety for our users, and block. We can always un-block if a user requests it. 

## Steps

1. If the suggester is a community member, inform them that you have seen the suggestion and are investigating.
2. Investigate the suggestion.
  * This does *not* require the moderator to navigate to the instance in question: moderator safety is _also_ a priority.
  * Is the suggester a known community member in good standing?
  * Is the suggester a known-good block list?
  * Is the suggester a known bad actor?
  * Is the suggestion being discussed or recommended by many sources?
  * What kind of content is prompting the suggestion? Is it spam? Content against our rules?
3. If the suggestion is credible, block the domain.
  1. Navigate to [federation settings](https://hachyderm.io/admin/instances).
  2. Check if the domain is already moderated.
  3. If not, click `Add new domain block`
  4. Enter the domain. 
  5. Choose an appropriate Severity and Rejection options
    * For content that actively breaks our rules, choose `suspend`.
    * For content that may still have value to some users, such as spam or bot activity, choose `silence`
      * Usually, you'll also want to reject both `media files` and `reports`. Use your judgement here.
  6. Obfuscate the domain name for servers that warrant `suspend`.
  7. Add a private comment indicating the types of content that prompted the block, and any information from step (2) that would help explain any decisions.
  8. Add a public comment:
     * For suspensions, put "Rules Violation".
     * For silences, put "Spam" or "Bot Activity".
  9. Click "Create Block"
  10. Communicate to the suggester that you've taken action, and what action you've taken.
  11. Post in the `#🐘-hachyderm-mods` channel on discord that you've taken action, what action you've taken, and the reason.
