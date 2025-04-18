# Ansible-Playbook-for-Nginx
Directory Structure:
ansible-nginx-setup/
├── playbook.yml
└── inventory.ini
Key Script:
yaml
# playbook.yml
- hosts: webservers
  become: yes
  tasks:
    - name: Install Nginx
      apt:
        name: nginx
        state: present
    - name: Start Nginx
      service:
        name: nginx
        state: started
      
