# ansible-role-i2p
Ansible role to install and configure [i2p](https://geti2p.net) on Debian-like systems.

![ansible-lint](https://github.com/sleepy-nols/ansible-role-i2p/actions/workflows/ansible-lint.yml/badge.svg)
![push-galaxy](https://github.com/sleepy-nols/ansible-role-i2p/actions/workflows/ansible-galaxy-push-role.yml/badge.svg)
![Ansible Galaxy](https://img.shields.io/badge/Ansible_Galaxy-sleepy--nols.i2p-blue)

---
## Role Variables and Defaults

```yml
i2p_name: i2psvc
i2p_unix_user: "{{ i2p_name }}"
i2p_unix_group: "{{ i2p_name }}"
i2p_unix_home: "/home/{{ i2p_name }}"
```
Name of user, group and service. Only `i2p_name` should be changed.

```yml
i2p_config_apparmor_enable: true
```
Enable AppArmor protection.

```yml
i2p_config_daemon_enable: true
```
Run i2p as a daemon.

```yml
i2p_config_memory: 128
```
Maximum RAM in MB.

```yml
i2p_gpg_apt_key_url: "https://geti2p.net/_static/i2p-archive-keyring.gpg"
```
Url to the i2p apt signing key.

```yml
i2p_package_dependencies:
  - "python3-debian"
  - "gpg"
```
Package dependencies, which the remote needs.

---
## Installing

Install via Ansible Galaxy or clone the Repo
```
ansible-galaxy role install sleepy-nols.i2p

git clone git@github.com:sleepy-nols/ansible-role-i2p.git
```
---
## Example Playbook

```yml
- hosts: i2p
  roles:
    - sleepy-nols.i2p
```

---
## Contributing

All contributions on are welcome. :)

---
## License
GPLv3
