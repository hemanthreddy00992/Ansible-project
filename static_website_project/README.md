## static website playbook

creating an Ansible playbook for deploying a static website involves automating the setup of an Apache web server and copying the static HTML files to a remote server. 

Inventory File: Define your server(s) in an inventory file (hosts), specifying the IP addresses or domain names of your remote servers.

Playbook Structure:

Tasks: Define tasks to achieve your goals. Tasks typically include:
Installing Apache: Use the ansible.builtin.apt module depending on your Linux distribution to ensure Apache is installed and running.
Copying HTML files: Use the copy module to transfer your index.html to the appropriate directory on the server (/var/www/html for Apache).
Setting permissions: Use the file or acl module to set appropriate permissions on your HTML files and directories.

<img width="1440" alt="Screenshot 2024-06-26 at 8 21 46 PM" src="https://github.com/hemanthreddy00992/Ansible-project/assets/130210051/f3eeccd4-bdd1-4a56-990a-359a798ea77f">
