# Ansible Role: system-watch

Installs system-watch monitoring on Debian and Ubuntu servers.

## Example Playbook

```yaml
    - hosts: all

      vars:
        system_watch_repo: ssh://git@git.yourserver.com/log.git
        system_watch_git_status_repos:
          - name: project1
            path: /srv/project1
          - name: project2
            path: /srv/project2

      roles:
        - alphanodes.tasks.system_watch
```

## Ignoring volatile lines

Some services rewrite generated values in their config files on their own
schedule. Those rewrites are no config change, but they still produce a commit
on every run. `system_watch_strip_lines` removes such lines from the synced
copies, so the file stays under version control while the noise is gone.

```yaml
    system_watch_strip_lines:
      - path: etc/letsencrypt/renewal
        patterns: '*.conf'
        lines:
          - '^\[acme_renewal_info\]$'
          - '^ari_retry_after = '
```

`path` is relative to the tracked host directory, `patterns` and `recurse` are
passed to `find` and default to `*` and `false`. Keep the path in
`system_watch_ls_options` as well - otherwise the changing mtime of the source
file still shows up in `etc_metadata.txt`.
