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
- SUSE Linux Enterprise 15<sup>1</sup>
- openSUSE Leap 15
- Debian 11 (Bullseye)
- Debian 12 (Bookworm)
- Ubuntu 20.04 LTS
- Ubuntu 22.04 LTS
- Fedora 37
- Fedora 38

Note:
<sup>1</sup> : no automated testing is performed on these platforms

## Role Variables
### defaults/main.yml
<pre><code>
# Default to fall back onto
firewalld_unsupported: true

# interfaces in trused zone
firewalld_trusted_interfaces: []
</pre></code>

### defaults/family-Debian.yml
<pre><code>
firewalld_packages:
  - firewalld
  - python3-firewall
</pre></code>

### defaults/family-Suse.yml
<pre><code>
firewalld_packages:
  - firewalld
  - python3-firewall
</pre></code>

### defaults/family-RedHat.yml
<pre><code>
firewalld_packages:
  - firewalld
  - python3-firewall
  - firewalld-filesystem
</pre></code>

### defaults/family-RedHat-7.yml
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
