# Ansible Role: LXC-Backup

Run LXC instance backups on Debian and Ubuntu servers.

## Dependencies

Installed LXC

## Installation

### Ansible 2+

Using ansible galaxy cli:

```shell
ansible-galaxy install alphanodes.lxc_backup
```

## Example Playbook

```yaml
    - hosts: server-name
      vars:
        lxc_backup_sets:
          - name: instance1
            with_stop: true
          - name: instance2
            with_stop: false
      roles:
        - alphanodes.lxc_backup
```

## License

GPL Version 3

## Author Information

This role was created in 2018 by [AlphaNodes](https://alphanodes.com/).
