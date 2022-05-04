# Runbook: Maintenance

This runbook captures the steps that should be followed when performing regular maintenance.

## Steps

1. Confirm that no-one else is "in session" working on the server
2. Alert [#hachyderm-infra](https://discord.com/channels/858148454953254943/970021502164557876). Include:
    * the maintenance you are planning
    * when you will start
    * how long you expect it to take
    * when you expect the service to be available again
3. Send an [announcement](https://hachyderm.io/admin/announcements) to users. Include:
    * when the maintenance period will start
    * how long you expect it to take
    * when you expect the service to be available again
4. Backup the ZFS volumes
    * run `sudo /home/novix/zfs/run-snap-create`
5. Do the thing!
6. If the thing is taking longer than you thought:
    * update [#hachyderm-infra](https://discord.com/channels/858148454953254943/970021502164557876)
    * alert [#hachyderm-mods](https://discord.com/channels/858148454953254943/970025957404581958) so they can field any user questions
7. When the thing is done, update [#hachyderm-infra](https://discord.com/channels/858148454953254943/970021502164557876). Include:
    * what you did
    * if anything unexpected came up
8. _maybe.. i'm not sure how this works_. Remove the [announcement](https://hachyderm.io/admin/announcements) to users.
