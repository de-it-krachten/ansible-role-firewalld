[![CI](https://github.com/de-it-krachten/ansible-role-firewalld/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-firewalld/actions?query=workflow%3ACI)


# ansible-role-firewalld

Install & configure firewalld


Platforms
--------------

Supported platforms

- CentOS 7
- CentOS 8
- Ubuntu 18.04 LTS
- Ubuntu 20.04 LTS
- Debian 10 (Buster)
- Debian 11 (Bullseye)



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

- name: Converge
  hosts: all
  tasks:

    - name: "Include role 'ansible-role-firewalld'"
      include_role:
        name: "ansible-role-firewalld"
</pre></code>
