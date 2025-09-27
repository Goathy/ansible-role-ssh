# Ansible Role: SSH
Configure `sshd` server according to [CISOfy Software - Lynis](https://cisofy.com/lynis/) benchmark.

> [!CAUTION]
> This role is in preview state. It will includes breaking changes without further notice.

Requirements
------------

This role only is needed/runs on RHEL and its derivatives.

Role Variables
--------------
```yaml
sshd_protocol: [2]

sshd_listen_address:
  - { address: "0.0.0.0", port: 22 }

ssh_deny_users: []
ssh_allow_users: [root]
ssh_deny_groups: []
ssh_allow_groups: [root, wheel]
```

Dependencies
------------

None.

Example playbook
----------------

License
-------

[MIT](./LICENSE)

Author Information
------------------

This role was created in 2014 by [Jakub Gałecki](https://github.com/Goathy).
