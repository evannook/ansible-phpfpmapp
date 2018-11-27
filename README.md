php_fpmapps
===========

Setup multi php fpm apps

Role Variables
--------------

```yaml
php_fpmapps_web_base_dir: YOUR_WEB_BASE_DIR (default: /srv/www)
php_fpmapps_vars:
  - domain_name: PHP_FPMAPP_DOMAIN_NAME
    base_dir: PHP_FPMAPP_BASE_DIR
    scm: PHP_FPMAPP_SCM_TOOLS (git or hg)
    repo_url: PHP_FPMAPP_REPO_URL
```

Dependencies
------------

- pylabs.php
- pylabs.add_ssh_known_hosts

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - role: pylabs.php_fpmapps
  vars:
    php_fpmapps_vars:
      - domain_name: www.example.com
        base_dir: /srv/www/example_com
        scm: git
        repo_url: https://github.com/pylabs/example_com
      - domain_name: www.example.org
        base_dir: /srv/www/example_org
        scm: hg
        repo_url: https://github.com/pylabs/example_org
```

License
-------

MIT

Author Information
------------------

William Wu
