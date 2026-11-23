## Access

Kanzo has no login of its own. Everyone allowed by the YunoHost permission can read and edit all boards. By default, that is every YunoHost user. To change it, go to Users > Groups and permissions in the admin. Do not make the app public.

## Data and logs

Boards live in `__DATA_DIR__` and are included in YunoHost backups. Logs: `journalctl -u __APP__`.

AI agents cannot use Kanzo's `/mcp` endpoint, because it is behind the YunoHost login.
