# Ansible Role: LXC-Backup

Run LXC instance backups on Debian and Ubuntu servers.

## Dependencies

Installed LXC

## Example Playbook

```yaml
    - hosts: all

      vars:
        lxc_backup_sets:
          - name: instance1
            with_stop: true
          - name: instance2
            with_stop: false
      roles:
        - alphanodes.tasks.lxc_backup
```
