### Heads-up / limitations in this draft

- **Single instance** only for now. Upstream services bind fixed local ports (3000/6042). Multi‑instance would require per‑instance port remapping & service templating.
- **Subdomain-only**: websockets over subpaths are finicky; this draft forces path=/.
- **Elasticsearch** is **optional** but strongly recommended for performance and advanced features. This draft suggests using an *external* ES ≥7.8,<9. Local ES on the same host is possible but heavy (RAM). OpenSearch is currently not wired.
- **SSO/LDAP**: not integrated yet. Use Zammad’s own user DB for first run.
- **Architectures**: amd64 only (per upstream packages). ARM64 would require Docker-based packaging instead.
- **Email**: you still need to configure inbound/outbound email channels in Zammad after install.
