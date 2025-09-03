# Ansible Playbooks

This repository was created for a test assignment.

---

## Key Components

### site.yml
The main entry point playbook.  
Defines which roles are applied to which hosts. You normally run this file when applying changes.

### roles/
Reusable Ansible roles:
- **support-tools** – installs helper utilities (e.g. `htop`).
- **nginx-conf** – prepare nginx.conf

### inventories/
Defines the infrastructure layout and variables:
- **dev/** – example development inventory with host definitions.
- **group_vars/** – variables shared within a host group.  
  Sensitive values can be stored in `vault.yml` and encrypted with Ansible Vault.  
- **host_vars/** – host-specific variables (e.g. SSH user, port, private key).

### ansible.cfg
Configuration file that controls Ansible behavior (e.g. defaults, SSH args).
