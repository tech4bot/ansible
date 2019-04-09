# How to use ansible

# install ansible on Debian:
sudo apt update
sudo apt install ansible

------

# ssh to servers without pass:
ssh-keygen - generate key
ssh-copy-id ansible@server1 - copy key to server
sudo adduser ansible - create ansible user
usermod -aG sudo username - grant sudo
sudo visudo
    add to the end of file:  
           ansible ALL=(ALL) NOPASSWD:ALL - allow deployment without asking for password


------

# create new role:
ansible-galaxy init *role*

# run playbook:
ansible-playbook -i inventories/test_env/hosts test.yml

------

