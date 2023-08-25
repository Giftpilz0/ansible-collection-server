# Ansible - cockpit

\=========

## Role Variables

______________________________________________________________________

| Variables                               | Type   | Options                                        | Defaults       |
| --------------------------------------- | ------ | ---------------------------------------------- | -------------- |
| cockpit_service_name:                   | string | ---                                            | cockpit.socket |
| cockpit_service_state:                  | string | reloaded, restarted, started, stopped          | started        |
| cockpit_service_enabled:                | bool   | false, true                                    | true           |
| cockpit_package_state:                  | string | present, absent, latest                        | present        |
| cockpit_package:                        | list   | ---                                            | ---            |
|                                         |        |                                                |                |
| cockpit_additional_package:             | dict   | ---                                            | ---            |
| cockpit_additional_package.package:     | string | ---                                            | ---            |
| cockpit_additional_package.requirement: | string | ---                                            | ---            |
| cockpit_additional_package.state:       | string | present, absent, latest, skip                  | present        |
|                                         |        |                                                |                |
| cockpit_firewalld_zone:                 | string | block, dmz, drop, internal, public, trusted... | ---            |
| cockpit_firewalld_service:              | string | ---                                            | cockpit        |
| cockpit_firewalld_state:                | string | present, absent, enabled, disabled, skip       | present        |

## Dependencies

______________________________________________________________________

## Example Playbook

______________________________________________________________________

### Basic

```
- name: Import cockpit Role
  hosts: all
  roles:
    - role: giftpilz0.server.cockpit
```
