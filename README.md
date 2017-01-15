# Ansible role: macOS Dock items

[![Build Status](https://travis-ci.org/danbohea/ansible-role-dock-items.svg?branch=master)](https://travis-ci.org/danbohea/ansible-role-dock-items)

Control which apps appear in your macOS Dock and in what order.


## Requirements

- macOS 10.10, 10.11 or 10.12


## Role Variables

All role default variables are listed below along with their respective default values.

```
dock_apps:
  - Google Chrome.app
  - Calendar.app
  - System Preferences.app
  - Terminal.app
```

A list of apps that you wish to appear in your Dock and in what order. You must include the `.app` extension. Only apps that are present directly within /Applications and optionally one level further down will be added (so apps located in /Applications/Utilities should work).


## Dependencies

None.


## Example Playbook

```
- hosts: macbook
  connection: local

  roles:
    - role: ansible-role-dock-items
```


## License

MIT


## Author Information

This role was created by [Dan Bohea](http://bohea.co.uk) primarily for use with [Macsible](https://github.com/macsible/macsible).
