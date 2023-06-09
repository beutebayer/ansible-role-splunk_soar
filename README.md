# ansible-role-splunk_soar
[![CI](https://github.com/beutebayer/ansible-role-splunk-soar/workflows/CI/badge.svg)](https://github.com/beutebayer/ansible-role-splunk-soar/actions/workflows/ci.yml?query=workflow%3ACI) 

A ansible role to install [Splunk SOAR](https://www.splunk.com/en_us/products/splunk-security-orchestration-and-automation.html)

## Requirements

This role is developed and tested for RHEL 8.x

## Role Variables

See also `defaults/main.yml`

```
splunk_soar_unix_user: soar
splunk_soar_unix_group: soar
splunk_soar_home: /opt/soar
splunk_soar_port: 8443

splunk_soar_tgz: "{{ splunk_soar_tgz_url | regex_search('\/([^\/]+.tgz)$', '\\1') | first }}"
```

This variable has to be set:

```
splunk_soar_tgz_url:
```

## Dependencies

None.

## Example Playbook

```
- hosts: soar-server
  roles:
    - beutebayer.splunk_soar
```

## License

MIT

## Author Information

Created by [beutebayer](https://github.com/beutebayer)
