Cisco Vlans
=========

Role for configuring vlans on Cisco network devices. Currently supports NX-OS only

This role will configure the vlan ids on the host, set their name and set the state to active by default

Requirements
------------

Ansible version 2.5 or greater.

Role Variables
--------------

The hosts that run this role should have the following configured:

```yaml
vlan_config:
  - vlan_id:  #number#
    name:     #name#
```

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: leaf_switches
  roles:
      - role: cisco_vlans
        vlan_config:
          - { vlan_id: 1, name: default_vlan }
          - { vlan_id: 2, name: inside_vlan }
```

License
-------

MIT
