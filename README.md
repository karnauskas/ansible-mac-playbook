Mac OS X playbook
=================

A playbook to configure OS X machine with Development and Operations / Administration tools.

# Requirements

First you need to install [homebrew](http://brew.sh/), the playbook will then update when there is an update.

Then you need to install Ansible if you are running the playbook locally, Ansible version needs to be 2.0 or greater.

__NOTE:__ _Check available version, and you can use `--devel` to install latest development version_

```bash
brew install ansible
brew install python
pip install ansible
```

# Provisioning Mac OS X, Configure & Install

```bash
ansible-playbook -i inventories/personal playbook.yaml --ask-become-pass -D
```

## Upgrade packages

```bash
ansible-playbook -i inventories/personal playbook.yaml --ask-become-pass -D -e pkg_state=latest
```

[![Analytics](https://ga-beacon.appspot.com/UA-45599204-2/README.md)](https://github.com/pmarques/ansible-mac-playbook)
