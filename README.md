# Ansible Collection - alphanodes.tasks

[![alphanodes.tasks.backup](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/backup.yml/badge.svg)](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/backup.yml)
[![alphanodes.tasks.drupal_task](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/drupal_task.yml/badge.svg)](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/drupal_task.yml)
[![alphanodes.tasks.git_mirror](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/git_mirror.yml/badge.svg)](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/git_mirror.yml)
[![alphanodes.tasks.git_rollout](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/git_rollout.yml/badge.svg)](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/git_rollout.yml)
[![alphanodes.tasks.jekyll_rollout](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/jekyll_rollout.yml/badge.svg)](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/jekyll_rollout.yml)
[![alphanodes.tasks.lxc_backup](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/lxc_backup.yml/badge.svg)](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/lxc_backup.yml)
[![alphanodes.tasks.matomo_task](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/matomo_task.yml/badge.svg)](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/matomo_task.yml)
[![alphanodes.tasks.nextcloud_task](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/nextcloud_task.yml/badge.svg)](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/nextcloud_task.yml)
[![alphanodes.tasks.project_sync](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/project_sync.yml/badge.svg)](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/project_sync.yml)
[![alphanodes.tasks.redmine_task](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/redmine_task.yml/badge.svg)](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/redmine_task.yml)
[![alphanodes.tasks.sphinx_rollout](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/sphinx_rollout.yml/badge.svg)](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/sphinx_rollout.yml)
[![alphanodes.tasks.system_task](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/system_task.yml/badge.svg)](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/system_task.yml)
[![alphanodes.tasks.system_watch](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/system_watch.yml/badge.svg)](https://github.com/alphanodes/ansible-collection-tasks/actions/workflows/system_watch.yml)

## Description

This collection provides tasks for:

- Linux operating systems:
  - Debian 11/12/13
  - Ubuntu 22.04/24.04

## Minimum required Ansible-version

- Ansible >= 2.15.0

## Included content

- [alphanodes.tasks.backup](roles/backup/)
- [alphanodes.tasks.drupal_task](roles/drupal_task/)
- [alphanodes.tasks.git_mirror](roles/git_mirror/)
- [alphanodes.tasks.git_rollout](roles/git_rollout/)
- [alphanodes.tasks.jekyll_rollout](roles/jekyll_rollout/)
- [alphanodes.tasks.lxc_backup](roles/lxc_backup/)
- [alphanodes.tasks.matomo_task](roles/matomo_task/)
- [alphanodes.tasks.nextcloud_task](roles/nextcloud_task/)
- [alphanodes.tasks.project_sync](roles/project_sync/)
- [alphanodes.tasks.redmine_task](roles/redmine_task/)
- [alphanodes.tasks.sphinx_rollout](roles/sphinx_rollout/)
- [alphanodes.tasks.system_task](roles/system_task/)
- [alphanodes.tasks.system_watch](roles/system_watch/)

## Installation

Install the collection via ansible-galaxy:

`ansible-galaxy collection install alphanodes.tasks`

or use latest (unreleased) version from git with:

`ansible-galaxy collection install git+https://github.com/alphanodes/ansible-collection-tasks.git,main`

## Using this collection

Please refer to the examples in the readmes of the role.

See [Ansible Using collections](https://docs.ansible.com/ansible/latest/user_guide/collections_using.html) for more details.

## Contributing to this collection

See the [contributor guideline](CONTRIBUTING.md).

## Licensing

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

<http://www.apache.org/licenses/LICENSE-2.0>

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
