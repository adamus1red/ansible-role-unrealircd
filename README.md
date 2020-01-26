UnrealIRCd [![Build Status](https://travis-ci.org/WhatsCS/ansible-role-unrealircd.svg?branch=master)](https://travis-ci.org/WhatsCS/ansible-role-unrealircd)
=========

This role will download and install the most recent version of UnrealIRCd.

Requirements
------------

None

Role Variables
--------------

|    Role Variable   |  Value |        Default        |                           Description                          |
|:------------------:|:------:|:---------------------:|:--------------------------------------------------------------:|
|      irc_user      | string |         ircd          |                    User to install server as                   |
|  unreal_build_dir  | string | /tmp/unrealircd-build |              Directory that the server is built in             |
|   unreal_version   | string |        '5.0.2'        |                       UnrealIRCd version                       |
| unreal_install_dir | string |      ~/unrealircd     |                        Install location                        |
| unreal_remote_conf |   int  |           1           | Whether or not to allow remote configs Accepted Values: 0 or 1 |
|   unreal_curl_dir  | string |          /usr         |             Location where curl libs are installed             |
|   unreal_ssl_dir   | string |                       |              SSL key directory, empty by default.              |

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - whatscs.unrealircd
      vars:
        unreal_install_dir: "/home/irc"
        remote_conf: 1  # 1 or 0


License
-------

BSD
