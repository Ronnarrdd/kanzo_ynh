## Access control

Kanzo has **no login of its own**: anyone who reaches the page can read and edit every board. Access is controlled only by the YunoHost permission. By default it is set to all YunoHost users. Never make it public. To restrict it further, go to Users > Groups and permissions in the admin.

## Files

- Binary: `__INSTALL_DIR__/kanzo`
- Data: `__DATA_DIR__/kanzo.db` (SQLite) and `__DATA_DIR__/config.toml`
- Logs: `journalctl -u __APP__`

`config.toml` is managed by the package. A manual edit is backed up on the next upgrade, but then replaced by the packaged version.

## Limits

- The `/mcp` endpoint is behind the YunoHost SSO, so an external AI agent cannot reach it without a session.
- Backups copy `kanzo.db` while the service runs. Stop the service (`sudo systemctl stop __APP__`) before a backup if you need a guaranteed consistent database, or use `kanzo export`.
- Kanzo's own sharing features (`kanzo share`, `kanzo sync`) are not integrated.
