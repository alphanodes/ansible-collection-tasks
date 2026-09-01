# Changelog

## 1.1.0

- project_sync: support managed databases (e.g. Google Cloud SQL) for PostgreSQL
  with `db_source_login_*`, `db_target_login_*` and `db_become_user`
- project_sync: molecule scenario covers the local and remote sync paths with a
  second container as sync source
- backup: use `login_port` instead of the deprecated `port` alias, which is
  removed in community.postgresql 5.0.0
- backup: molecule scenario covers the PostgreSQL dumps over unix socket and
  over tcp and verifies the created backups

## 1.0.1

- linter cleanup for [empty-string-compare](https://ansible.readthedocs.io/projects/lint/rules/empty-string-compare/)
- when conditions refactored with `and` logic

## 1.0.0

- merge of existing roles to a collection
