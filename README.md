## requirements ##
- Python3.9+
- docker
- docker-compose 2.x+ (Lower versions seem to work but not correctly with ansible)

---

## How to ##
This repository was made as a practice to start 3 containers (mssql, jenkins and workspace) using docker-compose with ansible.
The idea is to deploy containers using ansible by modifying the required files.

---

## How to add a new container to the list ##
Modify the vars inside the ansidocks role with the expected / needed parameters.
Create a new dockerfile inside ansidocks/files/container_folder/Dockerfile with the information you need.
Create a Python virtual environment and install ansible with pip.

---

## Create && start containers ##

Once you did everything mentioned above. Just go ahead and run:
- ansible-playbook install-me.yml

You'll find your new containers on the ./containers/ folder as default.

## How to delete && clean up everything ##
- ansible-playbook stop-me.yml

This playbook will STOP AND DELETE all containers by deleting the ./containers/ folder. BE AWARE.
