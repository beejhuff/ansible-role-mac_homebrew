Mac Homebrew
=========

[![Build Status](https://travis-ci.org/unfinisheddev/ansible-role-mac_homebrew.svg?branch=master)](https://travis-ci.org/unfinisheddev/ansible-role-mac_homebrew)

Ansible role to install Homebrew for Mac OS X. Does not install any binaries through Homebrew except Homebrew Cask if requested

Requirements
------------

* git

Role Variables
--------------

The path to install Homebrew to.  
Defaults to /usr/local - the same as the Homebrew installer provided on the website  
`mac_homebrew_install_path: /usr/local`                                           
                                                                                
The name of the binary that will be added to the path for running Homebrew       
`mac_homebrew_binary_name: brew`
                                                                              
Should we update the git repository if Homebrew is already installed?  
This is the same result as running `brew update` from the command line  
`mac_homebrew_force_update: no`
                                                                          
Should we install Homebrew Cask  
`mac_homebrew_install_cask: no`

Dependencies
------------

None

Example Playbook
----------------
```
- hosts: servers
  roles:
    - { role: unfinisheddev.mac_homebrew, mac_homebrew_install_cask: yes }
```

License
-------

BSD

