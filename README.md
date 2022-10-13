# **Ansible Role:** Zabbix Agent (Windows)

[![License](https://img.shields.io/badge/License-MIT-green?sytle=flat)](LICENSE)

## Description

This role downloads, installs and configures the Zabbix Agent (or Zabbix Agent 2) on Windows.

## Requirements

Ansible modules from the collections below are utilized. Ensure there is a requirements file if they are not already available.

```yaml
# Example /roles/requirements.yml
---
collections:
  - community.windows
```

## Role Variables

The values for default variables are listed below (see [`defaults/main.yml`](defaults/main.yml)). Ensure they are overwritten with the values you require. See [here](https://docs.ansible.com/ansible/latest/user_guide/playbooks_variables.html#variable-precedence-where-should-i-put-a-variable) for guidence on variable placement.

```yaml
zbx_agent2: false         # Zabbix agent 2 is a new generation of Zabbix agent and may be used in place of Zabbix agent
zbx_agent_release: 6.2.3  # See https://www.zabbix.com/download_agents for valid/latest release versions
zbx_server: 192.168.1.1   # IP addr or FQDN of the Zabbix server
zbx_passive_port: 10050   # Zabbix server will request agent on this port
zbx_active_port: 10051    # Active agent will request Zabbix server on this port
download_dest: '%USERPROFILE%\Downloads'     # Direcotry for the downloaded Zabbix agent .zip archive
install_dest: 'C:\zabbix'                    # Directory for the Zabbix agent executables and .conf files
```

## Dependencies

None

## Example Playbook

```yaml
- hosts: all
  roles:
    - lpwoodhouse.zabbix-agent-win
```

## Author Information

Created in 2022 by [Lee Woodhouse](https://www.leewoodhouse.com/).

[![Linkedin Badge](https://img.shields.io/badge/-LeeWoodhouse-0A66C2?style=flat&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/lee-woodhouse-58056118b/)](https://www.linkedin.com/in/lee-woodhouse-58056118b/)
[![Reddit Badge](https://img.shields.io/badge/-lpwoodhouse-FF4500?style=flat&logo=Reddit&logoColor=white&link=https://www.reddit.com/user/lpwoodhouse)](https://www.reddit.com/user/lpwoodhouse)
[![Twitter Follow](https://img.shields.io/twitter/follow/babswoodhouse?style=social)](https://twitter.com/intent/follow?screen_name=babswoodhouse/)
