# systemd

[![Build Status](https://travis-ci.com/daixijun/ansible-role-systemd.svg?branch=master)](https://travis-ci.com/daixijun/ansible-role-systemd)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-daixijun.systemd-660198.svg?style=flat)](https://galaxy.ansible.com/daixijun/ansible-role-systemd/)
[![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/daixijun/ansible-role-systemd?sort=semver)](https://github.com/daixijun/ansible-role-systemd/tags)

通过 systemd 管理进程

## 环境要求

- Ansible 2.9
- Centos 7+

## 角色变量

```yaml
systemd_services: []
# - name: example
#   description: ""
#   documentation: ""
#   type: simple
#   exec_start: /bin/cat
#   exec_reload: /bin/kill -HUP $MAINPID
#   exec_stop: /bin/kill $MAINPID
#   working_directory: /tmp
#   user: nobody
#   group: nobody
#   pid_file: ""
#   restart: on-failure
#   after: ""
#   wants: ""
#   requires: ""
#   wanted_by: "multi-user.target"
```

## 依赖

无

## 样例

```yaml
---
- name: Converge
  hosts: all
  tasks:
    - name: "Include daixijun.systemd"
      include_role:
        name: "daixijun.systemd"
      vars:
        systemd_services:
          - name: app
            exec_start: /usr/local/bin/app

```

## License

BSD

## 维护者

- Xijun Dai <daixijun1990@gmail.com>
