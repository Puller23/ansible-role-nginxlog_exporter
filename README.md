Ansible Role: nginxlog exporter
=========

Deploy prometheus [nginxlog exporter](https://github.com/martin-helmich/prometheus-nginxlog-exporter) using ansible.

Requirements
------------

- Ansible >= 2.7

Role Variables
--------------

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) and are listed in the table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `nginxlog_exporter_version` | 0.9.0 | nginxlog exporter package version.|
| `nginxlog_exporter_install_dir` | "" | Allows to use local packages instead of ones distributed on github.|
| `nginxlog_exporter_listen_adress` | "0.0.0.0" | Address on which nginxlog exporter will listen |
| `nginxlog_exporter_listen_port` | 4040 | Port on which nginxlog exporter will listen |
| `nginxlog_exporter_metrics` | "metrics" | Path under which to expose metrics |
| `nginxlog_exporter_system_user` | "nginx" | User for systemd service |
| `nginxlog_exporter_system_group` | "nginx" | User for systemd service |


Dependencies
------------

none

Example Playbook
----------------

Use it in a playbook as follows:
```yaml
- hosts: all
  roles:
    - puller23.nginxlog_exporter
```

License
-------

MIT

Author Information
------------------

This role was created in 2021 by Gregor Bartels.