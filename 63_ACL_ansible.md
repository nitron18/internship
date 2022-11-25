# Managing ACLs using Ansible
```
cd /home/thor/ansible

ansible all -a "ls -ltr /opt/security/" -i inventory
```
```
vi playbook.yml
```
```
- name: Create file and set ACL in Host 1

  hosts: stapp01

  become: yes

  tasks:

    - name: Create the blog.txt on stapp01

      file:

        path: /opt/security/blog.txt

        state: touch

    - name: Set ACL for blog.txt

      acl:

        path: /opt/security/blog.txt

        entity: tony

        etype: group

        permissions: r

        state: present

- name: Create file and set ACL in Host 2

  hosts: stapp02

  become: yes

  tasks:

    - name: Create the story.txt on stapp02

      file:

        path: /opt/security/story.txt

        state: touch

    - name: Set ACL for story.txt

      acl:

        path: /opt/security/story.txt

        entity: steve

        etype: user

        permissions: rw

        state: present

- name: Create file and set ACL in Host 3

  hosts: stapp03

  become: yes

  tasks:

    - name: Create the media.txt on stapp03

      file:

        path: /opt/security/media.txt

        state: touch

    - name: Set ACL for media.txt

      acl:

        path: /opt/security/media.txt

        entity: banner

        etype: group

        permissions: rw

        state: present
```
```
ansible-playbook -i inventory playbook.yml

ansible all -a "ls -ltr /opt/security/" -i inventory
```
