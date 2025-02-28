# Ansible Cheatsheet

## **Ansible Overview**
Ansible is an open-source automation tool used for configuration management, application deployment, and task automation.

---

## **Ansible Installation & Version Check**
```sh
ansible --version                 # Check installed Ansible version
ansible-galaxy --version          # Check Ansible Galaxy version
```

---

## **Ansible Inventory Management**
```sh
ansible-inventory --list          # List inventory hosts
ansible-inventory --graph         # Display inventory in graph format
```

---

## **Running Ansible Ad-hoc Commands**
```sh
ansible all -m ping                # Ping all hosts in inventory
ansible all -m shell -a 'uptime'    # Run shell command on all hosts
ansible <host_group> -m command -a 'df -h'  # Run a command on a specific group
```

---

## **Ansible Playbook Commands**
```sh
ansible-playbook <playbook.yml>    # Run a playbook
ansible-playbook <playbook.yml> --check  # Perform a dry run
ansible-playbook <playbook.yml> --syntax-check  # Validate syntax
ansible-playbook <playbook.yml> --list-tasks  # List tasks without executing
```

---

## **Working with Modules**
```sh
ansible-doc -l                      # List all available modules
ansible-doc <module_name>            # Show documentation for a module
```

---

## **Managing Variables & Facts**
```sh
ansible <host_group> -m setup        # Gather system facts
ansible-playbook <playbook.yml> --extra-vars "key=value"  # Pass extra variables
```

---

## **Managing Roles**
```sh
ansible-galaxy init <role_name>      # Create a new Ansible role
ansible-galaxy install <role>        # Install a role from Ansible Galaxy
```

---

## **Using Ansible Vault (Secret Management)**
```sh
ansible-vault create <file.yml>      # Create a new encrypted file
ansible-vault encrypt <file.yml>     # Encrypt an existing file
ansible-vault decrypt <file.yml>     # Decrypt an encrypted file
ansible-vault edit <file.yml>        # Edit an encrypted file
ansible-playbook <playbook.yml> --ask-vault-pass  # Run a playbook with encrypted vars
```

---

## **Ansible Configuration & Debugging**
```sh
ansible-config dump                  # Show current configuration
ansible-config list                   # List all configuration options
ansible -vvvv <host_group> -m ping    # Run a command with verbose debugging
```

---

## **Useful Ansible Resources**
- [Ansible Official Docs](https://docs.ansible.com/)
- [Ansible Galaxy](https://galaxy.ansible.com/)
- [Ansible Best Practices](https://docs.ansible.com/ansible/latest/user_guide/playbooks_best_practices.html)

---

This cheatsheet provides a quick reference for working with Ansible efficiently. Let me know if you have any suggestions or improvements!

