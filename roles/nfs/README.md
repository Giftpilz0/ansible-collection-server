# Ansible - nfs

\=========

## Role Variables

______________________________________________________________________

| Variables              | Type   | Options                                        | Defaults     |
| ---------------------- | ------ | ---------------------------------------------- | ------------ |
| nfs_service_name:      | list   | ---                                            | ---          |
| nfs_service_state:     | string | reloaded, restarted, started, stopped          | started      |
| nfs_service_enabled:   | bool   | false, true                                    | true         |
| nfs_package_state:     | string | present, absent, latest                        | present      |
| nfs_package:           | list   | ---                                            | ---          |
|                        |        |                                                |              |
| nfs_exports:           | dict   | ---                                            | ---          |
| nfs_exports.path:      | string | ---                                            | ---          |
| nfs_exports.host:      | string | ---                                            | ---          |
| nfs_exports.options:   | string | ---                                            | ---          |
| nfs_exports_state:     | string | present, absent, skip                          | present      |
| nfs_exports_file:      | string | ---                                            | /etc/exports |
|                        |        |                                                |              |
| nfs_firewalld_zone:    | string | block, dmz, drop, internal, public, trusted... | ---          |
| nfs_firewalld_service: | string | ---                                            | nfs          |
| nfs_firewalld_state:   | string | present, absent, enabled, disabled, skip       | present      |

## Dependencies

______________________________________________________________________

## Example Playbook

______________________________________________________________________

### Basic

```
- name: Import nfs Role
  hosts: all
  roles:
    - role: giftpilz0.server.nfs
```
