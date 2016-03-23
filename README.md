Role Name
=========

A simple Role to deploy an application.


Requirements
------------

Role Variables
--------------

* `deploy_path`: path to deploy to
* `deploy_owner`: owner of the deploy directory / files
* `deploy_group`: group of the deploy directory / files
* `deploy_release_file`: path to an archive with the release to deploy
* `deploy_shared_folders`: list with folders that are shared between releases e.g. sessions, logs, uploads

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: basserselim.deploy
           deploy_path: "/srv/app"
           deploy_release_file: "../release.tar.gz"
           deploy_owner: "www-data"
           deploy_group: "www-data"
           deploy_shared_folders:
             - path: "data/uploads"
               src: "uploads"
           # creates the direcotry /srv/app/shared/uploads if not exisiting and 
           # creates a link from /srv/app/current/data/uploads to /srv/app/shared/uploads


License
-------

BSD

Author Information
------------------

