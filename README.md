# Zammad for YunoHost (draft)

- Install: copy this folder to a Git forge and run

```bash
yunohost app install https://<your-git>/zammad_ynh --debug
```

- After installation: visit `https://<domain>` to run the setup wizard. If you enabled Elasticsearch, set its URL and rebuild the index from CLI:

```bash
zammad run rails r "Setting.set('es_url','http://<es-host>:9200')"
zammad run rake zammad:searchindex:rebuild
```

- Backup/restore: uses upstream scripts under `/opt/zammad/contrib/backup` and integrates with YunoHost backups.

- Remove: purges the APT package and removes the repo entry.
