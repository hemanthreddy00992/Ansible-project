# Security patchs for UBUNTU and Ansible Linux

1. This playbook uses Ansible to automate the patching process for security updates on Ubuntu and Amazon Linux machines.
2. It begins by updating the package cache (apt or yum) and then applies security patches (apt or yum) to ensure all packages are up to date. 
3. Tasks are structured to run on both Ubuntu and Amazon Linux using conditionals (when) based on distribution facts (ansible_distribution). 
3. The playbook ensures compliance and system security by verifying the successful application of updates (shell or command modules for verification). 
