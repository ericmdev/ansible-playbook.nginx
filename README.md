## Ansible: NGINX

[Ansible](http://www.ansible.com/) **playbook** to provision [NGINX](https://www.nginx.com/) web servers.

By default, the playbook provisions a `web` node in the `webservers` group:

    nginx_user: "nginx"
    nginx_vhosts:
      + listen: "80 default_server"
        server_name: "example.com"
        root: "/srv/app"
        index: "index.html"

*OS*
- RHEL/CentOS 6.x.

### Roles

- ca-certificates
- git
- libselinux-python
- nginx
- repo-epel-release
- repo-webtatic
- vim

### Clone

Clone repo:
    
    $ git clone <repo> ./ansible-playbook-nginx

### Installation

Ansible Galaxy install requirements.

    $ sh bin/install

### Usage

Vagrant up.

    $ vagrant up
