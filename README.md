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

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Usage
-----

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

``` yaml
- hosts: servers
    roles:
        - { role: username.rolename, x: 42 }
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
