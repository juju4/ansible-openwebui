[![Actions Status - Master](https://github.com/juju4/ansible-openwebui/workflows/AnsibleCI/badge.svg)](https://github.com/juju4/ansible-openwebui/actions?query=branch%3Amain)
[![Actions Status - Devel](https://github.com/juju4/ansible-openwebui/workflows/AnsibleCI/badge.svg?branch=devel)](https://github.com/juju4/ansible-openwebui/actions?query=branch%3Adevel)

# Open-webui ansible role

Ansible role to setup [Open-webui](https://github.com/open-webui/open-webui).

See also
* https://openwebui.com/
* https://docs.openwebui.com/
* https://pypi.org/project/open-webui/

Pip module has a [long dependency chain](https://github.com/open-webui/open-webui/blob/main/pyproject.toml#L8) and can take time to install depending on target system and network: 80+ modules (310 at the end from `pip freeze`), disk ~10GB.

## Requirements & Dependencies

### Ansible
It was tested on the following versions:
 * 2.10-17

### Operating systems

Tested on Ubuntu 24.04, 22.04, 20.04, Centos/Rockylinux 9.

## Example Playbook

Just include this role in your list.
For example

```
- host: myhost
  roles:
    - juju4.openwebui
```

you probably want to review variables

## Variables

TBD


## Continuous integration

```
$ pip install molecule docker
$ molecule test
$ MOLECULE_DISTRO=ubuntu:24.04 molecule test --destroy=never
```


## Troubleshooting & Known issues

* Pending PRs: [feat: add audit logging feature #8509](https://github.com/open-webui/open-webui/pull/8509)

## License

BSD 2-clause
