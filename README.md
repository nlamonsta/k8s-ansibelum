


## Prerequisites
1. A Linux computer (VM or physical) with the required KVM/libvirt components installed (kvmhost). --> https://linuxhint.com/install-kvm-ubuntu-22-04/
2. Ansible binaries installed on the controller machine. --> https://docs.ansible.com/ansible/latest/installation_guide/installation_distros.html
3. An intermediate level of domain (Ansible, KVM/libvirt, Kubernetes) knowledge.

## Code
1. Ansible roles were employed to keep tasks simpler and more organized. 
2. The Ubuntu 20.04 cloud image is downloaded and customized accordingly using virt-customize.
3. As for customization, configuration files (under kvmhost_scripts directory) and SSH keys were copied, root passwords were set.
4. community.libvirt.virt module was used to manage KVM VMs.
5. XML definition files under templates directory were used to boot up the VMs.
6. Four VMs were defined (HAProxy Load Balancer, master and two workers).
7. After starting the VMs, initialization scripts (under kvmhost_scripts directory) were run to bootstrap K8S cluster.
8. Resulting topology is given below.
