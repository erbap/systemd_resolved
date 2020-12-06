systemd_resolved
================

This Ansible role configure the systemd-resolved

**Note:** This role is still in active development. There may be unidentified issues and the role variables may change as development continues.

This role is developed wit ansible version 2.9.7


## Role Variables

[Variable explanaion](https://www.freedesktop.org/software/systemd/man/systemd-resolved.service.html)

### `systemd_resolved_servers:`

### `systemd_resolved_fallback_servers:`

### `systemd_resolved_domains:`

### `systemd_resolved_llmnr:`

### `systemd_resolved_multicast_dns:`

### `systemd_resolved_dnssec:`

### `systemd_resolved_dns_over_tls:`

### `systemd_resolved_cache:`

### `systemd_resolved_dns_stub_listener:`

### `systemd_resolved_read_etc_hosts:`


## example playbook

vi play_systemd_resolved.yml
```
---
- hosts: all
  become: True

  vars:
    systemd_resolved_servers: "8.8.8.8"
    systemd_resolved_domains: "example.com"
    systemd_resolved_cache: True
    systemd_resolved_read_etc_hosts: True

  roles:
  - { role: erbap.systemd_resolved }
...
```

## License

BSD-2-Clause-Patent

Like MIT and BSD-2-Clause and unlike Apache License v2, BSD+Patent is compatible with GPLv2.

Like Apache License v2 and unlike MIT and BSD-2-Clause, BSD+Patent avoids leading to potential patent trolls.
