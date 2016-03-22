Role Name
=========

A simple Role to deploy an application.


Requirements
------------

Role Variables
--------------
release_file: path to an archive with the release to deploy
run_user: the user who should own the app-directory
run_group: the group who should own the app-directory


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: basserselim.deploy, release_file: '../release.tar.gz', run_user: 'www-data', run_group: 'www-data' }

License
-------

BSD

Author Information
------------------

