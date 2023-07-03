# Ansible Role: redmine-task

Run Redmine tasks for an installed redmine (rake tasks)

- send reminder mails
- receive helpdesk mails (redmine_contacts)
- receive redmine mails
- run automation tasks (with AlphaNodes redmine_automation)
- maintenance tasks (see https://www.redmine.org/projects/redmine/wiki/RedmineRake)
- update or rebuild search index (for PostgreSQL) (https://github.com/AlphaNodes/redmine_postgresql_search)

## Dependencies

An installed redmine.

## Installation

### Ansible 2+

Using ansible galaxy cli:

```shell
ansible-galaxy install alphanodes.redmine_task
```

## Example Playbook

```yaml
    - hosts: server-name
      vars:
        redmine_task_name: reminder
      roles:
        - alphanodes.redmine_task
```

## License

GPL Version 3

## Author Information

This role was created in 2018 by [AlphaNodes](https://alphanodes.com/).
