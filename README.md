
Manage IPTables (IPv4) Firewalls Using Ansible
=======================

This role will manage IPTables firewalls on CentOS 6 or 7 servers, as well as Ubuntu, using Jinja templates and group / host vars.

Examples of **group_vars** and **host_vars** are included for reference.

Message that firewall was changed will be sent to Slack

Requirements
------------

You must have Ansible 2.0 installed.

You need a Slack server

You must be cool with **not using firewalld**

Examples
--------

To set firewall on a host:

```
ansible-playbook iptables.yml -e hosts=host --sudo -K
```

Notes
--------
The role will restart fail2ban gracefully as well as manage NFS and Samba firewall rules within Ipset.

All incoming and outgoing traffic on IPv6 networks will be dropped by default.

All unicast TCP and UDP packets will be looged in syslog
