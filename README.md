sbog/fluentd
============

Role to install and configure fluentd.

#### Requirements

Ansible 2.4

#### Role Variables

```yaml
fluentd_plugins: []
fluentd_config:
  - directive: system
    data:
      - |
        process_name: fluentd
        log_level: warning
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
