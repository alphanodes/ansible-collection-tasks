# Ansible Role: project-sync

Sync database (postgresql or mysql) and files between environments (e.g. production, staging etc.)

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

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
