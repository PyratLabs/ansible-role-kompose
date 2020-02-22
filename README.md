# Ansible Role: kompose

Ansible role for installing Kompose.

[![Build Status](https://www.travis-ci.org/PyratLabs/ansible-role-kompose.svg?branch=master)](https://www.travis-ci.org/PyratLabs/ansible-role-kompose)

## Requirements

This role has been tested on Ansible 2.7.0+ against the following Linux Distributions:

  - Amazon Linux 2
  - CentOS 8
  - CentOS 7
  - Debian 10
  - Fedora 29
  - Fedora 30
  - Fedora 31
  - Ubuntu 18.04 LTS

## Disclaimer

If you have any problems please create a GitHub issue, I maintain this role in
my spare time so I cannot promise a speedy fix delivery.

## Role Variables


| Variable              | Description                                                                  | Default Value    |
|-----------------------|------------------------------------------------------------------------------|------------------|
| `kompose_version`     | Use a specific version of Kompose, eg. `1.19.0`. Specify `false` for latest. | `false`          |
| `kompose_install_dir` | Installation directory for Kompose.                                          | `$HOME/bin`      |

## Dependencies

No dependencies on other roles.

## Example Playbook

Example playbook for installing to single user:

```yaml
- hosts: workstation
  roles:
     - { role: xanmanning.kompose, kompose_version: 1.6.2 }
```

Example playbook for installing the latest kompose version globally:

```yaml
---
- hosts: workstation
  become: true
  vars:
    kompose_install_dir: /opt/kompose/bin
  roles:
    - role: xanmanning.kompose
```

## License

[BSD 3-clause](LICENSE.txt)

## Author Information

[Xan Manning](https://xanmanning.co.uk/)
