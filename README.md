Role Name
=========

Install and configure firewall on RHEL based systems. 
The role abstracts the need to install and configure a firewall. Currently only iptables and firewalld are supported.

Requirements
------------

Ansible 1.4

Role Variables
--------------


  firewall_package_state: present
  firewall_service_state: running
  firewall_service_enabled: true
  firewall_config_services:
  - name: ssh
    state: enabled
  firewall_config_ports:
  - port: 123
    protocol: udp
    state: enable

dependencies
------------

No dependencies yet.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: firewall }

License
-------

BSD

Author Information
------------------

Thomas Krahn
