# About

[![Build status](https://github.com/rgl/my-openwrt-ansible-playbooks/workflows/build/badge.svg)](https://github.com/rgl/my-openwrt-ansible-playbooks/actions?query=workflow%3Abuild)

This is My OpenWrt Ansible Playbooks Playground.

This targets OpenWrt 22.03.

# Usage

Add your machines into the Ansible [`inventory.yml` file](inventory.yml).

Review the [`lab.yml` playbook](lab.yml).

See the facts about the `openwrt` machine:

```bash
./ansible.sh openwrt -m ansible.builtin.setup
```

Run an ad-hoc command in the `openwrt` machine:

```bash
./ansible.sh openwrt -a 'id'
```

Lint the `lab.yml` playbook:

```bash
./ansible-lint.sh --offline --parseable lab.yml
```

Run the `lab.yml` playbook against the `openwrt` machine:

```bash
./ansible-playbook.sh --limit=openwrt lab.yml
```
