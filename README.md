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

# Cipher algorithms approved by FIPS 140
sshd_cipher_algortihmss: ["aes256-gcm@openssh.com", "aes128-gcm@openssh.com", "aes256-ctr", "aes192-ctr", "aes128-ctr"]

# Key exchange algorithms approved by FIPS 140
sshd_key_exchange_algorithms: 
  - "ecdh-sha2-nistp256"
  - "ecdh-sha2-nistp384"
  - "ecdh-sha2-nistp521"
  - "diffie-hellman-group-exchange-sha256"
  - "diffie-hellman-group16-sha512"
  - "diffie-hellman-group18-sha512"
  - "diffie-hellman-group14-sha256"

# MACs algorithms approved by FIPS 140
sshd_mac_algorithms: ["hmac-sha1", "hmac-sha2-256", "hmac-sha2-512"]

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
