[![CI](https://github.com/de-it-krachten/ansible-role-firewalld/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-firewalld/actions?query=workflow%3ACI)


# ansible-role-firewalld

Install & configure firewalld


Platforms
--------------

Supported platforms

- CentOS 7
- CentOS 8
- RockyLinux 8
- AlmaLinux 8
- Debian 11 (Bullseye)
- Ubuntu 20.04 LTS



Role Variables
--------------
<pre><code>
# interfaces in trused zone
firewalld_trusted_interfaces:
  - docker0
</pre></code>


Example Playbook
----------------

<pre><code>
- name: sample playbook for role 'firewalld'
  hosts: all
  vars:
  tasks:
    - name: Include role 'firewalld'
      include_role:
        name: firewalld
</pre></code>
