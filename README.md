 Unbound DNS Resolver
======================

Ansible role to install and configure the `unbound` dns resolver.

Variables
---------

| variable | default | explaination |
| -------- | ------- | ------------ |
| ``unbound_listen_addresses:`` | ``['127.0.0.1@53','::1@53']`` | define interfaces and ports where unbound should listen |
| ``unbound__state:`` | ``present`` | Package state. *(use ``latest`` for explicit update)*
| ``submodules_versioncheck:`` | ``false`` | run basic versions check. ``true`` is recomended. |

 Files
-------

* `unbound.conf`:
  Main unbound configuration file.


 References
------------

* [Unbound Configuration](https://nlnetlabs.nl/documentation/unbound/unbound.conf/)
