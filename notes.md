## User and Database Creation

- Switched to postgres system user
- Created role with login privileges
- Created database owned by the new role
- Succesfully connected using psql

## PostgreSQL Configuration Directory

Path: /etc/postgresql/16/main

Main configuration files:
- postgresql.conf: General server configuration
- pg_hba.conf: Client authentication rules
- pg_ident.conf: User mapping

## Permissions note

- Access to /var/lib/postgresql/* is restricted
- Only the postgres system user can access the data directory
- This is a security measure to protect database files

## PostgreSQL Configuration (postgresql.conf)

- Configuration file located at /etc/postgresql/16/main/postgresql.conf
- Reviewed important parameters such as listen_addresses and port
- Enabled DDL logging by setting log_statement = 'ddl'
- Restarted PostgreSQL service to apply changes

## PostgreSQL Logs

- Log directory: /var/log/postgresql/
- Main log file: postgresql-16-main.log
- Reviewed logs using tail
- Confirmed DDL logging after configuration change

## Backup and Restore

- Created logical backup using pg_dump
- Backup stored as SQL file
- Database dropped and recreated 
- Backup succesfully restored
