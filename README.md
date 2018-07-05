Ansible Role to Install Libvirt
=========

Ansible role to install Libvirt.

Role Variables
--------------

Variables are defined in `defaults/main.yml` and structured/encapsulated in `vars/`.

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `autorun` | `False`  | Boolean to define if the role "autorun" (`tasks/main.yml`). Useful when you want to have dependencies solved by galaxy (`meta/main.yml`) but don't want it to run automatically.  |
| `libvirt_auth_group` | `libvirt` | Group allowed to connect to libvirt via polkit. |
| `libvirt_services_state` | `started`  | The services state: started, stopped or restarted |
| `libvirt_services_enabled` | `yes` | Bool to define if services shall start on-boot. |

Examples
------------

Follow below different examples and ways to use this role.

>Playbook: Install Libvirt with default options.

```YAML
---
- name: "libvirt: Install libvirt"
  hosts: network_lab
  gather_facts: true
  become: true

  roles:
    - role: victorock.libvirt
      autorun: true

```

License
------------

GPLv3

Author
------------

Victor da Costa (@victorock)
