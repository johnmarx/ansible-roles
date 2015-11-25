# Akema ansible roles

add submodule in roles/ folder

    mkdir deployment
    cd deployment
    git submodule add git@github.com:11h42/ansible-roles.git roles
    git submodule update --init

copy default-playbook.yml

    cp roles/default-playbook.yml ${app_name}.yml
    
modify variables in the playbook to meet your need. Tip: try to remove all comment

    edit ${app_name}.yml

deploy your application (be sure you can ssh to your server and run)

    ansible-playbook --ask-sudo-pass -i '192.168.5.x,' ${app_name}.yml
   
# Adding specific roles

create a file named `ansible.cfg` containing:

    [defaults]
    roles_path = ./local-roles

create a folder `local-roles` and put your custom roles into

# Roles working with FreeBSD (10.x) and Ubuntu (14.04)

  * python-virtualenv

# todo

  * fix roles to work with FreeBSD


  
