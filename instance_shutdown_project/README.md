# Instance shutdown

1. Inventory: Define EC2 instances in the inventory file.
2. Playbook Setup: Specify gather_facts: true to gather instance facts.
3. Condition: Use when condition with ansible_distribution == 'Ubuntu'.
4. Task: Include ec2 module with state: stopped to shut down Ubuntu instances.
5. Execution: Run with ansible-playbook shutdown_playbook.yml -i inventory.
