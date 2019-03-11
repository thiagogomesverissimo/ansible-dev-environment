## ansible dev environment

This repo contains some files organized to speed up the setup of the 
environment to develop my ansible roles using virtualbox and vagrant

Download it (I prefer not to clone due to I use this repo only as base to develop roles):

    wget https://github.com/thiagogomesverissimo/ansible-dev-environment/archive/master.zip
    unzip master.zip
    mv ansible-dev-environment-master developing-awesome-role

Up VMs:

    vagrant up debian
    vagrant up ubuntu

Create roles folder and clone ansible roles repos inside it:

    mkdir roles
    cd roles
    git clone YOUR-ROLE

Edit the playbook.yml to fit your needs and be happy:

    ansible-playbook playbook.yml

