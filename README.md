Role Name
=========

This role automated the process of installing Cache on a Linux machine unattended.

Requirements
------------

It is assumed that Cache is to be installed on either a Red Hat or SuSE derived system as adviced by Intersystems

Role Variables
--------------

package - The architecture of the linux environment. Can be one of:

lnxrhx64 - Red Hat Enterprise Linux (x64)
lnxrhx86 - Red Hat Enterprise Linux (Intel)
lnxsusex64 - SuSE Linux Enterprise Server (x64)
lnxsusex86 - SuSE Linux Enterprise Server (Intel)

[ Default - lnxsusex86 ]

instname - The name of the Cache instance to install

[ Default - TEST ]

inst_dir - Where to install the Cache

[ Default - /usr/local/cache ]

mangrp - The management group to run Cache under

[ Default - cacheusr ]

cspbool - Whether to install Cache Server Page or not (Y or N)

[ Default - Y ]

servtyp - What type of web stack you are running (either Apache of Nginx)

[ Default - Apache ]

csp_dir - Where to install Cache Server Pages (CSP)

[ Default - /opt/cspgateway ]

key_bool - Whether you have a Cache key/licence file to copy (Y or N) If Y then you must pass the variable key_lock which should contain the location of the key file on the local server

[ Default - N ]
Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      role: cache
      platform: lnxrhx86
      instname: CACHE
      ...

License
-------

BSD

Author Information
------------------

Raman Sailopal
