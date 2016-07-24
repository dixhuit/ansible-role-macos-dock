# Ansible role: macOS Dock items

[![Build Status](https://travis-ci.org/danbohea/ansible-role-dock-items.svg?branch=master)](https://travis-ci.org/danbohea/ansible-role-dock-items)

Control which apps appear in your Dock and in what order.

## Requirements

- macOS 10.10+


## Role Variables

All role default variables are listed below along with their respective default values.

```
dock_apps:
  - Google Chrome.app
  - Calendar.app
  - Atom.app
  - Wunderlist.app
  - System Preferences.app
```

A list of apps that you wish to appear in your Dock and in what order. You must include the `.app` extension. Only apps that are present within /Applications will be added.

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

This role was created by [Dan Bohea](http://bohea.co.uk) primarily for use with [Macsible](https://github.com/danbohea/macsible).
