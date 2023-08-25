# Ansible - pcp

\=========

## Role Variables

______________________________________________________________________

| Variables            | Type   | Options                               | Defaults |
| -------------------- | ------ | ------------------------------------- | -------- |
| pcp_service_name:    | list   | ---                                   | ---      |
| pcp_service_state:   | string | reloaded, restarted, started, stopped | started  |
| pcp_service_enabled: | bool   | false, true                           | true     |
| pcp_package_state:   | string | present, absent, latest               | present  |
| pcp_package:         | list   | ---                                   | ---      |

## Dependencies

______________________________________________________________________

## Example Playbook

______________________________________________________________________

### Basic

```
- name: Import pcp Role
  hosts: all
  roles:
    - role: giftpilz0.server.pcp
```
