# PostgreSQL Installation on Ubuntu Server 22.04 LTS

This document describes the installation and initial verification of PostgreSQL on Ubuntu Server 22.04 LTS.

## Environment

- Operating System: Ubuntu Server 22.04 LTS
- Virtualization: Oracle VirtualBox
- PostgreSQL Version: 16
- User: bastihan

## System Update

Before installing PostgreSQL, the system package index was updated:

```bash
sudo apt update
```

## PostgreSQL Installation

PostgreSQL and additional contributed utilities were installed using the default Ubuntu repositories:

```bash
sudo apt install postgresql postgresql-contrib
```

During the installation, no manual configuration was required.

## Version Verification

After installation, the PostgreSQL client version was verified:

```bash
psql --version 
```

This confirms that PostgreSQL was successfully installed.

## Service Status Check

PostgreSQL runs as a system service. Its status was verified using:

```bash
sudo systemctl status postgresql
```

The service should be shown as `active (running)`.

## Accessing PostgreSQL

PostgreSQL uses a dedicated system user named `postgres`.  
To access the PostgreSQL shell:

```bash
sudo -i -u postgres
psql
```

A successful connection displays the PostgreSQL prompt:

```text
postgres=#
```

## Initial Verification

The list of existing databases was checked:

```sql
\l
```

This confirms that the PostgreSQL server is operational and accepting connections.

## Exit

To exit the PostgreSQL shell and return to the normal user:

```sql
\q
```

```bash
exit

```
