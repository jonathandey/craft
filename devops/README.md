# Craft DevOps

### Ansible

```
ansible-galaxy install -r requirements.yml
```

#### Webserver

This script will:

1. Turn on Unattended-Updates
1. Install, enable & configure UFW (open ports 22 (rate-limiting enabled), 80 & 443)
1. Create the "craft" user and home directory, as well as add the worker public key

```
ansible-playbook install-webserver.yml -i inventories/test
```

Todo

- [ ] Install Caddy Server
- [ ] Install PHP (allow for multiple versions & cli version)
- [ ] Install Mariadb
- [ ] Install Composer
- [ ] Install Supervisor
- [ ] Install redis
- [ ] Install restic (backups)
- [ ] Install & configure Logrotate
- [ ] Install MeiliSearch
- [ ] Install Postgres
- [ ] Install Memcached
- [ ] Install OPCache