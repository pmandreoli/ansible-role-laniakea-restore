Role Name
=========
Role to plant lanikaea flavor in a Galaxy-minimal instance.

### Flavor (currently) supported
- galaxy-rna-workbench  
- galaxy-testing

Requirements
------------

ansible 2.9 
tested on CentOS7

Role Variables
--------------

`galaxy_flavor`: galaxy-testing

Dependencies
------------
### Infrastructure:

**galaxy virtual machine:**
- deployed using the image `galaxy20_05lite` 
- with a volume mounted in `/export`  
this vm can be deployed on Openstack cloud  using the Terraform recipe at 
https://github.com/pmandreoli/TerraFormExpress

### Roles

- `galaxyproject.cvmfs` role

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
