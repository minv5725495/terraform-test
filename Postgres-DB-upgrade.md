# Consideration about upgrade from v11 to v16 

# swap

SWAP is Tier-1 service, it should be upgraded with minimal downtime

scenario:

- Drop the quotes table content - this will speed up dramatically step 3.
- Stop the completer, let the service run
- Copy the database
- Connect application to the copy of database
- Migrate the original database
- Connect application to the original database
- Restart the completer (and therefore the critical writes)


notify team-data

`team-data` use read replica to


since v15 postgres set default  parameter force_ssl = true.



