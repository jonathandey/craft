# Craft DevOps

### Ansible

This installation had been optimised for Ubuntu 20.04.

```
ansible-galaxy install -r requirements.yml
```

#### Webserver

This script will:

1. Turn on Unattended-Updates
1. Install, enable & configure UFW (open ports 22 (rate-limiting enabled), 80 & 443)
1. Create the "craft" user and home directory, as well as add the worker public key
1. Install caddy and host a holding page: "Hello world, from Craft!"

```
ansible-playbook install-webserver.yml -i inventories/test
```

Todo

- [x] Install Caddy Server
- [ ] Install PHP (allow for multiple versions & cli version)
- [ ] Install Mariadb
- [ ] Install Composer
- [ ] Install Supervisor
- [ ] Manage host sites
- [ ] Install Nodejs
- [ ] Install redis
- [ ] Install restic (backups)
- [ ] Install & configure Logrotate
- [ ] Install MeiliSearch
- [ ] Install Postgres
- [ ] Install Memcached
- [ ] Install OPCache