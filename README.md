# -Ansible-playbook
#  VM Provisioning & Guacamole Integration via Ansible

This Ansible playbook automates the process of:

 Cloning a base QCOW2 image  
 Spinning up a new KVM virtual machine  
 Setting up a cloud-init-based user config  
 Fetching the new VM's IP dynamically  
 Automatically registering the VM on [Apache Guacamole](https://guacamole.apache.org/) for SSH access

##  Requirements

- Ansible
- KVM / libvirt installed and configured
- `virt-install`, `virsh`, `qemu-img`, `cloud-localds`
- Guacamole server running on `localhost:8989`
- Internet access (for cloud-init updates if required)

---

## How to Use

### 1. Clone the Repo
```bash
git clone https://github.com/your-username/ansible-vm-guac-automation.git
cd ansible-vm-guac-automation
```
```bash
ansible-playbook provision_vm.yml
```
