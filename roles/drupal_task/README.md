# Ansible Role: drupal-task

Run Drupal task. This role does not configure the system environment for drush and Drupal.

List of possible tasks:

- rollout
  It just run the code rollout with optional drush commands as pre and/or post_commands. And a git pull to update code base.
- cron
  It run drupal cron with drush
- scheduler
  It run drupal schedule-cron with drush

List of possible rollout tasks:

- composer update
- git pull
- drush with updatedb
- drush with cache-clear
- drush with cron
- drush with cim

Supported are: Drupal 7 and Drupal 8

## Dependencies

Installed Drupal and drush

## Example Playbook

```yaml
    - hosts: server-name
      vars:
        drupal_task_name: rollout
        drupal_task_instance: drupal2
        drupal_instances:
          - name: drupal1
          - name: drupal2
          - name: drupal_another
      roles:
        - alphanodes.drupal-task
```

You have to use --extra-vars "drupal_task_instance=NAME"' to rollout a specific instance, if there are more than one instance on a host. For each Drupal instance, it is required that an drush profile already exists with the name of the Drupal instance (e.g. @drupal1, @drupal2 or @drupal_another)

## License

GPL Version 3

## Author Information

This role was created in 2018 by [AlphaNodes](https://alphanodes.com/).
