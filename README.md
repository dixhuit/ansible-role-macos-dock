# Ansible role: macOS Dock

[![Build Status](https://travis-ci.org/danbohea/ansible-role-dock-items.svg?branch=master)](https://travis-ci.org/danbohea/ansible-role-dock-items)

Configure the macOS Dock including which items appear in it and in what order.


## Requirements

- Ansible >= 2.1
- macOS 10.13, 10.12, 10.11 or 10.10


## Role Variables

```yaml

# Whether the Dock automatically hides.
macos_dock_autohide: true

# The size of icons in the Dock.
macos_dock_icon_size: 60

# The orientation of the Dock.
# "left | "bottom" | "right"
macos_dock_orientation: "bottom"

# A list of apps that you wish to appear in the Dock and in what order.
# 
# Supported directories for apps:
# - /Applications
# - /Users/[username]/Applications
# 
# Notes:
# - Use absolute paths to files.
# - List order affects order in Dock.
# - {{ ansible_user_id }} returns the username of the *target* system
#   (you must surround the path in quotes to use this).
#   
# Examples:
# - /Applications/System Preferences.app
# - /Applications/Utilities/Activity Monitor.app
# - "/Users/{{ ansible_user_id }}/Applications/Firefox.app"
macos_dock_apps: []

# Max directory depth when checking for installed apps.
macos_dock_apps_dir_maxdepth: 2

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
