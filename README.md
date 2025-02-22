Ansible Course Files Documentation
1. ansible.cfg
Description:
This configuration file defines global settings for Ansible. The [defaults] section includes host_key_checking = False, which disables SSH host key verification, preventing errors when connecting to new hosts.

2. inventory_table
Description:
This inventory file defines multiple hosts and groups for Ansible automation. It includes Linux (sql_db1, sql_db2) and Windows (web_node1, web_node2, web_node3) hosts with connection credentials. Hosts are grouped under [db_nodes], [web_nodes], [boston_nodes], [dallas_nodes], and [us_nodes].

3. inventory
Description:
This inventory file lists hosts and groups for Ansible. It defines two nodes (node01, node02) and groups them under [web_nodes].

4. banana.yml
Description:
This playbook checks if a given variable (fruit) is set to "banana." It executes different commands based on the condition, printing a message indicating whether it is a banana or not.

5. fruits.yml
Description:
This playbook prints a list of fruits by iterating over an array using the with_items loop. Each fruit name is printed in sequence.

6. command.yml
Description:
This playbook runs a command on the localhost to display the contents of the /etc/resolv.conf file. This can be useful for checking DNS configurations.

7. copy_file.yml
Description:
This playbook copies files to specific hosts with defined ownership and permissions. It applies conditional logic to determine which file to copy based on the inventory hostname.

8. copy.yml
Description:
This playbook copies a file from a source directory to a target directory on all hosts. It ensures the file exists at the destination.

9. file.yml
Description:
This playbook creates a file on node01 and writes specific content into it. The file will be managed by Ansible to ensure it exists with the defined content.

10. file_redirect.yml
Description:
This playbook creates a file on a target host and appends text to it using a handler. The handler is triggered after the file is created.

11. my_main-role.yml
Description:
This Ansible role installs and starts the Nginx service on target hosts. It ensures the web server is installed and running.

12. package.yml
Description:
This playbook installs the vim-enhanced package on the localhost using the YUM package manager. It ensures the package is present on the system.

13. prem.yml
Description:
This playbook creates empty files with specific ownership and permissions on different hosts. The first task creates blog.txt on node01, and the second creates story.txt on node02.

14. service.yml
Description:
This playbook installs the vsftpd package and ensures the service is started on all hosts. It automates the setup of the FTP server.

Now, the documentation follows a logical order:

Configuration File (ansible.cfg)
Inventory Files (inventory_table, inventory)
Basic Playbooks (banana.yml, fruits.yml, command.yml)
File and Copy Operations (copy_file.yml, copy.yml, file.yml, file_redirect.yml)
Roles & Package Management (my_main-role.yml, package.yml)
Permissions & Services (prem.yml, service.yml)
