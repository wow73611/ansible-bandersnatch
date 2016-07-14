About
=====

Deploy pip mirror and nginx service with [Ansible](https://www.ansible.com/).


Requirements
=====

- OS: Ubuntu 14.04 (trusty)
- [Ansible >= 2.0](https://github.com/ansible/ansible)


Usage
=====

Deploy with hosts file (Make sure hosts file is you need)
```
ansible-playbook -i hosts playbook.yml
```

Run as other users or use sudo
```
ansible-playbook -i hosts playbook.yml \
-e "ansible_ssh_pass=secret ansible_sudo_pass=secret sudo=yes"
```

Open your browser and go to:
```
http://<HOST-IP>/pypi/
```

Ansible Variables
=====

* pip_virtualenv_path: Virtual enviroment path (Default: /root/bandersnatch)
* pip_mirror_base_path: Base path of pip-mirror (Default: /srv/pypi)
* nginx_root_directory: Root directory of web service (Default: /usr/share/nginx/html)
