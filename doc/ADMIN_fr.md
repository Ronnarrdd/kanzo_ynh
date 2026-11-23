## Accès

Kanzo n'a pas de connexion propre : la permission YunoHost décide qui peut lire et modifier tous les tableaux. Par défaut, tous les utilisateurs YunoHost y ont accès. Pour changer cela : Utilisateurs > Groupes et permissions. Ne rendez pas l'application publique.

## Données et journaux

Les tableaux sont dans `__DATA_DIR__` et inclus dans les sauvegardes YunoHost. Journaux : `journalctl -u __APP__`.

Les agents IA ne peuvent pas utiliser `/mcp`, car il est derrière la connexion YunoHost.
