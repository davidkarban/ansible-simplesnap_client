Simplesnap_client
=========

Backup your ZFS machines by simplesnap. Role installs simplesnap client part onto your server and setup backup on the backup server.

Requirements
------------

Backup server needs to have simplesnap installed, best way for this role is by davidkarban.simplesnap_server, but can be any other working way.

Role Variables
--------------

simplesnap_backup_server:
  - backup server for host/group.


Example Playbook
----------------

group_vars/all:
simplesnap_backup_server: backup.domain.tld

    - hosts: all:!backup_servers
      roles:
         - { role: davidkarban.simplesnap_client }

License
-------

GPLv3

Author Information
------------------

David Karban

email: david@karban.eu

web: www.karban.eu

Jan Pechek

