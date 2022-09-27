ansible-role-tailscale
=========

<p align="center">

<a href="https://github.com/iancleary/ansible-role-tailscale/actions?query=workflow%3Aci" target="_blank">
    <img src="https://github.com/iancleary/ansible-role-tailscale/workflows/CI/badge.svg" alt="CI workflow status">
</a>

<a href="https://github.com/iancleary/ansible-role-tailscale/actions?query=workflow%3Arelease" target="_blank">
    <img src="https://github.com/iancleary/ansible-role-tailscale/workflows/Release/badge.svg" alt="Release workflow status">
</a>
<a href="https://galaxy.ansible.com/iancleary/tailscale" target="_blank">
    <img src="https://img.shields.io/badge/ansible--galaxy-iancleary.tailscale-blue.svg" alt="Ansible Galaxy">
</a>
<a href="https://raw.githubusercontent.com/iancleary/ansible-role-tailscale/main/LICENSE" target="_blank">
    <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License">
</a>
</p>

This role installs [Tailscale (A secure network that just works)](https://tailscale.com/download/linux), but **does not connect it to your Tailscale network**!

>After using this role, connect your machine to Tailscale.
>
>Login directly via ssh
>Connect your machine to your Tailscale network and authenticate in your browser:
>
>`sudo tailscale up`
>
>You’re connected! You can find your Tailscale IPv4 address by running:
>
>`tailscale ip -4`


Requirements
------------

Supported and Tested `ansible_os_families`:

* Ubuntu 22.04
* Ubuntu 20.04

> Pull Requests welcome!

Role Variables
--------------

There are no role variables used.


Dependencies
------------

N/A

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: servers
  user: unprivelaged
  roles:
    - role: iancleary.tailscale
      become: true
```

```yaml
- hosts: servers
  user: root
  roles:
    - role: iancleary.tailscale
```

License
-------

[MIT](LICENSE)

Author Information
------------------

This role was created in 2021 by [Ian Cleary](https://iancleary.me).

Inspiration for the structure of this repo came from [Jeff Geerling](https://github.com/geerlingguy/ansible-role-nginx).
