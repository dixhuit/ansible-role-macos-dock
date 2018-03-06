# Ansible role: macOS Dock

[![Build Status](https://travis-ci.org/danbohea/ansible-role-dock-items.svg?branch=master)](https://travis-ci.org/danbohea/ansible-role-dock-items)

Configure the macOS Dock including which items appear in it and in what order.


## Requirements

- Ansible >= 2.1
- macOS 10.10, 10.11 or 10.12


## Role Variables

```yaml

# The apps that you wish to appear in your Dock and in what order.
# Only apps that are present directly within /Applications and optionally one level further down will be added (so apps located in /Applications/Utilities should work).
# Note:
# - List order will effect order in Dock.
# - Filenames must include .app extension.
macos_dock_apps:
  - Activity Monitor.app
  - Firefox.app
  - Calendar.app
  - System Preferences.app
  - Terminal.app

# Whether the Dock automatically hides.
macos_dock_autohide: true

# The size of icons in the Dock.
macos_dock_icon_size: 60

# The orientation of the Dock.
# "left | "bottom" | "right"
macos_dock_orientation: "bottom"

```


## Dependencies

None.


## Example Playbook

```yaml
- hosts: all

  roles:
    - ansible-role-dock-items
```


## License

MIT


## Author Information

This role was created by [Dan Bohea](http://bohea.co.uk) primarily for use with [Macsible](https://github.com/macsible/macsible).
