Ansible Role: docker
-----

Supported distributions:
* ubuntu
* centos

This role installs docker and docker_container ansible module.


Example playbook
-----

```yaml
- hosts: prod
  become: true
  roles:
    - docker

  tasks:
    - name: "Launch nginx container"
      docker_container:
        name: webapp
        image: nginx
        ports:
          - "80:80"
```
