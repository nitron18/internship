# Using Ansible Conditionals
```
cd /home/thor/ansible/

ll

cat inventory

ansible all -a "ls -ltr /opt/dba" -i inventory

ll /usr/src/dba/
```
```
vi playbook.yml
```
```
- name: Copy text files to Appservers

  hosts: all

  become: yes

  tasks:

    - name: Copy blog.txt to stapp01

      ansible.builtin.copy:

        src: /usr/src/dba/blog.txt

        dest: /opt/dba/

        owner: tony

        group: tony

        mode: "0755"

      when: inventory_hostname == "stapp01"

    - name: Copy story.txt to stapp02

      ansible.builtin.copy:

        src: /usr/src/dba/story.txt

        dest: /opt/dba/

        owner: steve

        group: steve

        mode: "0755"

      when: inventory_hostname == "stapp02"

    - name: Copy media.txt to stapp03

      ansible.builtin.copy:

        src: /usr/src/dba/media.txt

        dest: /opt/dba/

        owner: banner

        group: banner

        mode: "0755"

      when: inventory_hostname == "stapp03"
```
```
ansible-playbook -i inventory playbook.yml
```
