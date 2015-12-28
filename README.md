Ansible: NGINX Webserver
=======================

Ansible playbook to provision nginx web servers.

By default, the playbook provisions a `web` node in the `webservers` group with the following nginx configuration declared in `group_vars/webservers.yml`:

    nginx_user: "nginx"
    nginx_vhosts:
      + listen: "80 default_server"
        server_name: "example.com"
        root: "/srv/app"
        index: "index.html"

OS:
- RHEL/CentOS 6.x.

Usage
-----

Clone repo:
    
    $ git clone <repo> ./ansible

Ansible Galaxy install requirements.

    $ ansible-galaxy install -r requirements.yml -p roles/ --ignore-errors

Vagrant
-------

Vagrant up:

    $ vagrant up
