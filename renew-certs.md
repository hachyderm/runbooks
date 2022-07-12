# Renew Let's Encrypt certs

To renew the certs manually:
```
[novix@alice]: ~>$ sudo ./zfs/run-zfs-snap-create
/sbin/zfs snapshot -r data@2022-07-12_13.39.54--1m ... DONE
[novix@alice]: ~>$ sudo certbot renew
```
