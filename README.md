sbog/fluentd
============

Role to install and configure fluentd.

#### Requirements

Ansible 2.4

#### Role Variables

```yaml
# true if td-agent v4 is installed on the host
fluentd_migrate_to_v5: false
fluentd_del_old_conf: false

# for ssl 
ssl_directory_path: "/etc/ssl_certs"
domain_directory: "example.com"

fluentd_plugins: []
fluentd_config:
  - directive: system
    data:
      - |
        process_name fluentd
        log_level warn
```

#### Dependencies

None

#### Example Playbook

```yaml
- name: Install and configure Fluentd
  hosts: localhost
  remote_user: root
  roles:
    - fluentd
```

#### License

Apache 2.0

#### Author Information

Stanislaw Bogatkin (https://sbog.ru)
