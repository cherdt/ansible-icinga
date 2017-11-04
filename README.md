# Playbook to help install Icinga 1.x on CentOS 7

Why? Because there are more pieces than you might think.

(Why not? Because Icinga 1.x is old and you should probably look at Icinga 2.x)

## Assumptions

* You have a vanilla install of CentOS 7.
* You've already run a `yum update` and `reboot`
* You've installed ansible: `yum install ansible`
* You've installed git: `yum install git`

## Usage

This Ansible playbook can be used to install Icinga 1.x on localhost. You are free to modify it to do other things of course.

* `git clone https://github.com/cherdt/ansible-icinga.git`
* `cd ansible-icinga`
* `ansible-playbook site.yml`
* `reboot`
* visit http://icingaadmin:icingaadmin@localhost/icinga/

## Known issues

There are problems if SELinux is in Enforcing mode. This playbook sets SELinux to Permissive mode, which is something you shouldn't do in a production environment.
