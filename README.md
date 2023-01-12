[![CI](https://github.com/de-it-krachten/ansible-role-firewalld/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-firewalld/actions?query=workflow%3ACI)


# ansible-role-firewalld

Install & configure firewalld



## Dependencies

#### Roles
None

#### Collections
- community.general
- ansible.posix

## Platforms

Supported platforms

- Red Hat Enterprise Linux 7<sup>1</sup>
- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- CentOS 7
- RockyLinux 8
- RockyLinux 9
- OracleLinux 8
- OracleLinux 9
- AlmaLinux 8
- AlmaLinux 9
- Debian 11 (Bullseye)
- Ubuntu 20.04 LTS
- Ubuntu 22.04 LTS
- Fedora 35
- Fedora 36

Note:
<sup>1</sup> : no automated testing is performed on these platforms

## Role Variables
### defaults/main.yml
<pre><code>
# interfaces in trused zone
firewalld_trusted_interfaces: []
</pre></code>


### vars/family-RedHat.yml
<pre><code>
firewalld_packages:
  - firewalld
  - python3-firewall
  - firewalld-filesystem
</pre></code>

### vars/default.yml
<pre><code>
firewalld_unsupported: true
</pre></code>

### vars/family-Debian.yml
<pre><code>
firewalld_packages:
  - firewalld
  - python3-firewall
</pre></code>

### vars/family-RedHat-7.yml
<pre><code>
firewalld_packages:
  - firewalld
  - python-firewall
  - firewalld-filesystem
</pre></code>



## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'firewalld'
  hosts: all
  become: "yes"
  tasks:
    - name: Include role 'firewalld'
      ansible.builtin.include_role:
        name: firewalld
</pre></code>
