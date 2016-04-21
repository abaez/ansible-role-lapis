Role Name
=========
[![license][2i]][2p]
[![twitter][3i]][3p]

A role to run lapis as a docker service.

Description
-----------

[Lapis][4] is a microframework built using [lua][5]. Very easy to use and quite fun to work with. This role allows you to have a working lapis environment through the combination of docker and systemd.

Role Variables
--------------

The role contains a couple of variables that are required to be changed to run properly:

``` rust
dir.app: String // directory of the lapis application.

vhost.name: String // a domain url for the lapis app.
vhost.port: u8 // a port number for the domain to bind to.

user.name: String // user who will run the systemd service of the container.
```

Requirements
------------

The roles required are listed below:

* [abaez.domain][6]
* [abaez.docker][7]

Usage
-----

Besides the role variables listed above, the only other piece required to run the role is to have required role added to the playbook.

``` yaml
- hosts: servers
    roles:
        - abaez.domain
        - abaez.docker
        - lapis
```

Author Information
------------------

[Alejandro Baez][1]

[1]: https://keybase.io/baez
[2i]: https://img.shields.io/badge/license-BSD_2-green.svg
[2p]: ./LICENSE
[3i]: https://img.shields.io/badge/twitter-a_baez-blue.svg
[3p]: https://twitter.com/a_baez
[4]: http://leafo.net/lapis
[5]: https://www.lua.org
[6]: https://galaxy.ansible.com/abaez/domain
[7]: https://galaxy.ansible.com/abaez/docker
