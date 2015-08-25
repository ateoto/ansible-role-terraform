terraform
=========

Installs and configures Hashicorp's Terraform tool. We use this role to install Terraform for use in Jenkins builds. It won't download/install anything if you already have terraform installed unless your installed version is older than the specified terraform_version.

Role Variables
--------------

You can specify a version, default is `0.6.3` by overriding `terraform_version`.

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
         - { role: ateoto.terraform }
```

To override the version to install:

```yaml
    - hosts: servers
      roles:
         - { role: ateoto.terraform, terraform_version: 0.6.2 }
```

Retention of older versions is not under our control, nor is it'

License
-------

MIT
