# Basic ansible use

## install ansible on Debian:
sudo apt update

sudo apt install ansible -y

## ssh to servers without pass:
### create ansible user(run on all servers)
sudo adduser ansible
### grant sudo (run on all servers)
usermod -aG sudo username
sudo visudo
>add to the end of file:

ansible ALL=(ALL) NOPASSWD:ALL
### generate key (run only from source)
ssh-keygen
### copy key to server (run only from source)
ssh-copy-id ansible@server1

----
### create new role:
ansible-galaxy init *role*

----
### run playbook:
ansible-playbook -i inventories/test_env/hosts playbook.yml
