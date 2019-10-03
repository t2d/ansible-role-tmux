ansible-role-tmux
=================

Setup a useable tmux config including dependencies on Debian-derivates.

* Use the great tmux config [gpakosz/.tmux](https://github.com/gpakosz/.tmux)
* Install pre-built version of [PathPicker](https://facebook.github.io/PathPicker/)

Role Variables
--------------

    tmux_packages:
      - tmux
      - urlview
    
    tmux_fpp_version: 0.9.2
    
    tmux_fpp_path: /root/
    
    # configure tmux for following users
    tmux_users: []
    
    # change tmux defaults
    tmux_defaults:
      - regexp: "^#?set -g mouse"
        line: "set -g mouse on"


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: ansible-role-tmux, tmux_users: vagrant }

License
-------

GPLv3
