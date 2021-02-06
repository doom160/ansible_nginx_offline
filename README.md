# Ansible playbook for deploying nginx server in disconnected env

## Task
1. Write an Ansible playbook required to deploy a basic Nginx web server on an on-prem server.
2. Assume that the on-prem server will not have access to the internet.

## Assumptions
1. Assuming all remote servers are running on ubuntu 64-bit OS
2. Executing host should have default ssh access, and no password authentication is require
3. It should have the basic OS packages
4. Installation guide are mostly referred from [official nginx guide] (https://docs.nginx.com/nginx/admin-guide/installing-nginx/installing-nginx-open-source/#sources) with slight modification

## Run
### Local run
1. Run following commands
`sudo ansible-playbook -i hosts --connection==local nginx_local.yml`

### Local run
1. Update `hosts` file for the list of webserver
2. Run following commands
`sudo ansible-playbook -i hosts nginx.yml`