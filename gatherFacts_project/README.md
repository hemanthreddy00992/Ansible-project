# Gathered Facts

 Purpose: The playbook collects system information (facts) from remote hosts using Ansible's setup module.


 Inventory: Define hosts in an inventory file (hosts) with their IP addresses or hostnames.


 Playbook Structure:
  
  1. Specify hosts and become root (become: yes) if necessary.
  
  2. Use the gather_facts: yes option to collect system information.
  
  3. Include tasks to display gathered facts using debug module (debug:) with msg parameter.


 Execution: Run playbook with ansible-playbook -i inventory.ini gatherfacts-playbook.yml.


 Output: Displays gathered facts such as OS version, IP addresses, CPU architecture, and more for each host specified in the inventory.


 Customization: Modify playbook to filter specific facts or format output as needed.


 Automation: Useful for inventory management, monitoring, or configuration validation across multiple servers.





