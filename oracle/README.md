# Oracle database

## Basic queries

```sql
-- Get available pluggable databases
SELECT NAME, OPEN_MODE FROM "GV$CONTAINERS";

-- Open a pluggable database
ALTER PLUGGABLE DATABASE FREEPDB1 OPEN;

-- Create tablespace
CREATE TABLESPACE my_tablespace
  DATAFILE '/opt/oracle/oradata/my_tablespace.dbf' SIZE 100M
  AUTOEXTEND ON NEXT 10M MAXSIZE 1G;

-- Create user
CREATE USER $username IDENTIFIED BY $password
  [DEFAULT TABLESPACE tablespace_name]
  [TEMPORARY TABLESPACE temp_tablespace_name]
  [QUOTA {size | UNLIMITED} ON tablespace_name]
  [PROFILE profile_name]
  [ACCOUNT {LOCK | UNLOCK}];
```
