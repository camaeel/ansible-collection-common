Install packages
=========

Handles package installation for debian based systems (using apt). Updates package cache, adds additional repositories, isntalls packages and removes obsolete packages.

Requirements
------------

Apt compatible linux system

Role Variables
--------------

- sources_keys - List of urls to gpg keys
- sources_repos - List of apt sources 
- add_packages_list - list of packages to install
- remove_packages_list - list of packages to remove
- clean_packages_cache - if packages cache should by cleaned

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
        - role: camaeel.common.install_packages
          add_packages_list:
          - curl
          remove_packages_list:
          - snapd
          sources_keys:
          - https://packages.cloud.google.com/apt/doc/apt-key.gpg
          sources_repos:
          - 'deb https://apt.kubernetes.io/ kubernetes-xenial main'
          

License
-------

Apache-2.0

Author Information
------------------

https://github.com/camaeel
