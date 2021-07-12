Role Name
=========
Role to plant lanikaea flavor in a Galaxy-minimal instance

Requirements
------------

ansible 2.9 
tested on CentOS7

Role Variables
--------------

`galaxy_flavor`: laniakea-galaxy-flavor

Dependencies
------------

`galaxyproject.cvmfs` role

Example Playbook
----------------


    ---
    
    - name: restore
      hosts: galaxy
      become: true
      vars:
        galaxy_flavor: galaxy-testing
      roles: 
        - ansible-role-laniakea-restore

License
-------

GNU General Public License v3.0

Author Information
------------------

author: Pietro Mandreoli
email: pietro.mandreoli@unimi.it
