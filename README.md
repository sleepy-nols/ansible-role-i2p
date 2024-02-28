# ansible-role-i2p
Ansible role to install and configure [i2p](https://geti2p.net) on Debian-like systems.

![ansible-lint](https://github.com/sleepy-nols/ansible-role-i2p/actions/workflows/ansible-lint.yml/badge.svg)
![push-galaxy](https://github.com/sleepy-nols/ansible-role-i2p/actions/workflows/ansible-galaxy-push-role.yml/badge.svg)
![Ansible Galaxy](https://img.shields.io/badge/Ansible_Galaxy-sleepy--nols.i2p-blue)

---
## Role Variables and Defaults


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
