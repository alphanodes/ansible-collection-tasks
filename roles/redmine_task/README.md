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

## Example Playbook

```yaml
    - hosts: all

      vars:
        redmine_task_name: reminder

      roles:
        - alphanodes.tasks.redmine_task
```
