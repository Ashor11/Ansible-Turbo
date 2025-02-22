# 📖 Ansible Course Files Documentation

## 📌 Configuration File  
### `ansible.cfg`  
This configuration file defines global settings for Ansible. The `[defaults]` section includes:  
- `host_key_checking = False` → Disables SSH host key verification to prevent connection errors with new hosts.  

---

## 📂 Inventory Files  
### `inventory_table`  
Defines multiple hosts and groups for Ansible automation. It includes:  
- **Linux hosts:** `sql_db1`, `sql_db2`  
- **Windows hosts:** `web_node1`, `web_node2`, `web_node3`  
- **Host groups:** `[db_nodes]`, `[web_nodes]`, `[boston_nodes]`, `[dallas_nodes]`, `[us_nodes]`  

### `inventory`  
Lists hosts and groups for Ansible. Defines:  
- **Nodes:** `node01`, `node02`  
- **Group:** `[web_nodes]`  

---

## 📜 Basic Playbooks  
### `banana.yml`  
Checks if a variable (`fruit`) is set to `"banana"`. Outputs a message based on the condition.  

### `fruits.yml`  
Loops through an array of fruits using `with_items`, printing each name sequentially.  

### `command.yml`  
Runs a command on `localhost` to display the `/etc/resolv.conf` file, useful for checking DNS configurations.  

---

## 📁 File & Copy Operations  
### `copy_file.yml`  
Copies files to specific hosts with defined ownership and permissions. Uses conditional logic based on the inventory hostname.  

### `copy.yml`  
Copies a file from a source directory to a target directory on all hosts, ensuring it exists.  

### `file.yml`  
Creates a file on `node01` with specific content, ensuring Ansible manages it consistently.  

### `file_redirect.yml`  
Creates a file on a target host and appends text using a handler. The handler triggers after the file is created.  

---

## 🛠️ Roles & Package Management  
### `my_main-role.yml`  
Installs and starts the **Nginx** service on target hosts, ensuring it is properly set up.  

### `package.yml`  
Installs the `vim-enhanced` package on `localhost` using the **YUM** package manager, ensuring the package is present.  

---

## 🔒 Permissions & Services  
### `prem.yml`  
Creates empty files with specific ownership and permissions:  
- `blog.txt` on `node01`  
- `story.txt` on `node02`  

### `service.yml`  
Installs the `vsftpd` package and ensures the service is started on all hosts, automating FTP server setup.  

---

## 📌 How to Use These Playbooks  
1. Ensure Ansible is installed on your system.  
2. Update the inventory file to match your environment.  
3. Run a playbook using:  
   ```sh
   ansible-playbook -i inventory <playbook_name>.yml
