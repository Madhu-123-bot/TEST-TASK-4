# TEST-TASK-4

Steps to Automate Nginx Installation
1.Clone the Repository

git clone https://github.com/yourusername/ansible_automation.git
cd ansible_automation

2.Edit the Inventory File
Update the inventory file with your EC2 instance details:

[web]
ec2_instance ansible_host=<EC2_PUBLIC_IP> ansible_user=ubuntu ansible_ssh_private_key_file=/path/to/your-key.pem

3.Run the Ansible Playbook
Execute the playbook to install Nginx:

ansible-playbook -i inventory nginx_install.yml

4.Verify Installation
Visit http://<EC2_PUBLIC_IP> in a browser to check Nginx.
Run the command below to confirm Nginx is active:

ansible -i inventory -m shell -a "systemctl status nginx" all
Push Changes to GitHub:

git add .
git commit -m "Added updates"
git push origin main


