# Ansible Role: redmine_fast_rollout

## Dependencies

An installed redmine.

## Example Playbook

```yaml
    - hosts: all

      vars:
        redmine_instances:
          redmine:

      roles:
        - alphanodes.tasks.redmine_fast_rollout
```
