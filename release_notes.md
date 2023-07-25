# What's New
This is the initial release of the `FortiManager ZTP Flow` (ZTPF) Solution Pack. 

# Known Bugs

## Dashboard Dynamic Content ( 0932566 )

If you are updating an exsiting solution pack then the included Announcment might be auto-incremented. This impacts the Dashboard Quick Links. To fix this SSH into FortiSOAR and run the following command until this is fixed. 

```
sudo env PGPASSWORD=$(cat /home/csadmin/device_uuid) psql -U cyberpgsql -d venom -c "update announcements set id=1 where uuid='83ca88a8-e02f-48a1-901f-39aede335b7d';"
```

See internal Bug ID `0932566` for latest status of the bug. 
