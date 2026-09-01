# Changelog

## 1.1.0

- project_sync: support managed databases (e.g. Google Cloud SQL) for PostgreSQL
  with `db_source_login_*`, `db_target_login_*` and `db_become_user`
- project_sync: molecule scenario covers the local and remote sync paths with a
  second container as sync source

## 1.0.1

- linter cleanup for [empty-string-compare](https://ansible.readthedocs.io/projects/lint/rules/empty-string-compare/)
- when conditions refactored with `and` logic

## 1.0.0

- merge of existing roles to a collection
