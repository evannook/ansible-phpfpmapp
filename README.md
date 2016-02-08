phpfpmapp
=========

Setup php-fpm app

Role Variables
--------------

```yaml
phpfpmapp_project_name: PHP_FPM_APP_PROJECT_NAME
phpfpmapp_domain_name: PHP_FPM_APP_DOMAIN_NAME
phpfpmapp_basedir: PHP_FPM_APP_BASE_DIR
phpfpmapp_scm: YOUR_SCM_TOOLS (git or hg)
phpfpmapp_repo: REPO_PATH
```

Dependencies
------------

- evannook.php

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - role: evannook.phpfpmapp
  vars:
    phpfpmapp_project_name: myproject
    phpfpmapp_domain_name: www.example.com
    phpfpmapp_basedir: /srv/www/myproject
    phpfpmapp_scm: git
    phpfpmapp_repo: https://github.com/evannook/test_project
```

License
-------

MIT

Author Information
------------------

Evan Nook
