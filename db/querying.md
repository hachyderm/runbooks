# Querying the Database

As an administrator, sometimes you'll need to query the database directly to do your job. In this doc, we'll stash our collective knowledge about working with the database.

## Working with pSQL

### Connecting

To connect, start by running `psql`:  

```bash
cd /var/lib/mastodon
sudo ./run-psql
```

which will drop you at a `psql` prompt:

```
psql (14.2)
Type "help" for help.

postgres=#
```

To connect to the mastodon database, you can then use `\c`:

```
postgres=# \c mastodon_production
You are now connected to database "mastodon_production" as user "postgres".
mastodon_production=#
```

### Disconnecting

Disconnect from the database using `\q`, which will drop you back to your shell:

```
mastodon_production=# \q
could not save history to file "/var/lib/postgres/.psql_history": No such file or directory
[novix@alice]: /var/lib/mastodon>$ 
```

## Queries

### Media Attachments

## Find statuses before X that have media attachments

```sql
select
    s.id
from
    statuses s
where
    exists
    (
        select
            *
        from
            media_attachments ma
        where
            ma.status_id = s.id
    )
    and s.created_at <= '2022-05-03 22:00:00';
```
