## my ansible dev environment

This repo contains some files organized to speed up the setup of the 
environment to develop my ansible roles using virtualbox and vagrant

Up VMs:

    vagrant up debian
    vagrant up ubuntu

Create roles folder and clone ansible roles repos inside it:

    mkdir roles
    cd roles
    git clone YOUR-ROLE

Edit the playbook to fit your needs and be happy:

    ansible-playbook playbook.yml

