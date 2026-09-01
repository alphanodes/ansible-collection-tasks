# Ansible Role: project-sync

Sync database (postgresql or mysql) and files between environments (e.g. production, staging etc.)

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

### Managed databases (PostgreSQL)

By default all PostgreSQL commands run as the local `postgres` system user
over the unix socket. Managed databases (e.g. Google Cloud SQL) have no such
user, so the connection settings have to be given per instance. Source
settings are used on `src_host`, target settings on the host this role runs
on:

- `db_become_user`: system user for PostgreSQL commands, set to `''` if there
  is no local `postgres` user
  (default: `project_sync_postgresql_become_user`)
- `db_source_login_host`: database host of the dump source, `pg_dump` connects
  over tcp if this is set
- `db_source_login_port`: database port of the dump source
- `db_source_login_user`: database user of the dump source
- `db_source_login_password`: database password of the dump source, passed to
  `pg_dump` via stdin
- `db_target_login_host`: database host of the sync target
- `db_target_login_port`: database port of the sync target
- `db_target_login_user`: database user of the sync target
  (default: `db_target_owner`)
- `db_target_login_password`: database password of the sync target

## Dependencies

rsync for file sync. If you want database sync, you need database packages (mysql or postgresql) of linux distribution

## Example Playbook

```yaml
- hosts: all

  vars:
    project_sync_instances:
      - name: prod-staging
        src_host: remote-prod.example.com
        src_dir: /srv/store/files
        target_parent_dir: /srv/store
        db_type: postgresql
        db_source_name: store
        db_target_name: store
        db_target_owner: store

  roles:
    - alphanodes.tasks.project_sync
```

if you have defined more the one instance and you only want a specific one to run, use --extra-vars "project_sync_instance_name=NAME"'
