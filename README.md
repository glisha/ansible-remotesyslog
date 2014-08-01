remotesyslog
============

Configures rsyslog on the server to send all logs to a central log server.

On a RHEL and derivate systems if SELinux is enforcing and a non standard
port is used it configures SELinux to allow rsyslog usage of that port.


Role Variables
--------------

- `remotesyslog_host` - The central log server hostname or ip. If an IPv6 ip enclose it in brackets.
- `remotesyslog_proto` - The protocol on the receiving log server (tcp,udp,relp). Default tcp.
- `remotesyslog_port` - The receiving port. Default 601.


Example Playbook
----------------

    - hosts: servers
      vars_files:
        - site_vars/remotesyslog.yml

      roles:
         - glisha.remotesyslog

Where site_vars/remotesyslog.yml is defaults/main.yml modifed to your needs.

License
-------

MIT

Author Information
------------------

Georgi Stanojevski
[GitHub project page](https://github.com/glisha/ansible-remotesyslog)
