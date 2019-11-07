freehck.k8s_base
=========

Deploy base kubernetes binaries

Description
-----------

This role installs `kubelet`, `kubeadm` and `kubectl`.

This role is a base block to deploy kubernetes base. After you apply this role, you'll need to initialize your cluster, deploy some CNI, and join nodes to cluster.

Role Variables
--------------

`k8s_base_node_ip`: ip address of this kubernetes node

`k8s_base_ver`: version of kubernetes binaries you want to install

Example
-------

    - hosts: all
      become: true
      vars:
        k8s_base_node_ip: "{{ ansible_host }}"
        k8s_base_ver: "1.16.2-00"
      roles:
        - role: freehck.k8s_base

Install
-------

This role can be installed from [Ansible Galaxy](https://galaxy.ansible.com/):

`ansible-galaxy install freehck.add_repo`

License
-------

MIT

Author Information
------------------

Dmitrii Kashin, <freehck@freehck.ru>

