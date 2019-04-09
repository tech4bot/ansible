# Basic ansible use

## install ansible on Debian:
sudo apt update

sudo apt install ansible -y

## ssh to servers without pass:
### generate key
ssh-keygen
### copy key to server
ssh-copy-id ansible@server1
### create ansible user
sudo adduser ansible
### grant sudo
usermod -aG sudo username
sudo visudo
*add to the end of file:*
### allow deployment without asking for password  
ansible ALL=(ALL) NOPASSWD:ALL

### create new role:
ansible-galaxy init *role*

### run playbook:
ansible-playbook -i inventories/test_env/hosts playbook.yml


