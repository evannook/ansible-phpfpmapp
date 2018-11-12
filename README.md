php_fpmapp
==========

Setup php fpm app

Role Variables
--------------

```yaml
php_fpmapp_project_name: PHP_FPMAPP_PROJECT_NAME
php_fpmapp_domain_name: PHP_FPMAPP_DOMAIN_NAME
php_fpmapp_basedir: PHP_FPMAPP_BASE_DIR
php_fpmapp_scm: YOUR_SCM_TOOLS (git or hg)
php_fpmapp_repo: REPO_PATH
```

Dependencies
------------

- pylabs.php

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - role: pylabs.php_fpmapp
  vars:
    php_fpmapp_project_name: myproject
    php_fpmapp_domain_name: www.example.com
    php_fpmapp_basedir: /srv/www/myproject
    php_fpmapp_scm: git
    php_fpmapp_repo: https://github.com/pylabs/test_project
```

License
-------

MIT

Author Information
------------------

William Wu
