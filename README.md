# tobias_richter.apt_cacher_ng

[![Build Status](https://github.com/tobias-richter/ansible-apt-cacher-ng/workflows/CI/badge.svg)](https://github.com/tobias-richter/ansible-apt-cacher-ng/actions)

This role setups a apt-cacher-ng instance using
[elnappo.apt_cacher_ng](https://galaxy.ansible.com/elnappo/apt-cacher-ng)
and enables you to configure:
* `passthroughpattern` and
* `precachefor`

## Requirements

This role requires Ansible 2.7 or higher.

## Role Variables

See [defaults/main.yml](defaults/main.yml) for the documented role variables.

## Example Playbook

This playbook setups the apt cacher and allows all repositories to pass through.

    - hosts: apt_cacher_ng
	  roles:
	    - role: tobias_richter.apt_cacher_ng
	      apt_cacher_ng_passthroughpattern: '.*'