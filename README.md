# Ansible playbook: Deploy nginx server in disconnected env

## Task
1. Write an Ansible playbook required to deploy a basic Nginx web server on an on-prem server.
2. Assume that the on-prem server will not have access to the internet.

## Assumptions
1. All remote servers are running on Ubuntu
2. Executing host should have default ssh access, and no password authentication is required
3. It should have the basic OS packages where no other additional packages required apart from those from nginx installation
4. Installation guide are mostly referred from [official Nginx installation guide](https://docs.nginx.com/nginx/admin-guide/installing-nginx/installing-nginx-open-source/#sources) with slight modification

## Local run
1. Run following commands\
`sudo ansible-playbook -i hosts --connection==local nginx_local.yml`

## Remote run
1. Update `hosts` file for the list of webserver
2. Run following commands\
`sudo ansible-playbook -i hosts nginx.yml`

## Result
![Ngingx](screenshots/nginx.jpg?raw=true "Nginx")