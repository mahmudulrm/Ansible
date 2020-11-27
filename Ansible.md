#Anible server 

rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm

echo "ansadmin    ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers

[all_hosts]
ip address
ip address



## Check ansible :

ansible all -m ping
ansible all -m copy -a "src=/home/ansadmin/test/index.html  dest=/home/ansadmin"
ansible docker -m copy -a "src=/home/ansadmin/test/index.html  dest=/home/ansadmin"

---
- hosts: web
  become: true	
  tasks:
  - name: copy war to the remote server
    copy:
      src: /opt/webfile/webapp/target/webapp.war
      dest: /opt/apache-tomcat-8.5.58/webapps


ansible-playbook /opt/playbooks/copyfile.yml

#Check ownership of your folder by running ls -ltr in your parent directory.
ls -ltr

sudo chown -R dockeradmin:dockeradmin /opt

give task 

ansible-playbook push_docker_version.yml --extra-vars "JOB_NAME=$JOB_NAME BUILD_ID=$BUILD_ID"


ansible-playbook test.yml --extra-vars "JOB_NAME=test BUILD_ID=10"

docker build -t java_demo_project /opt/docker
docker build -t {{JOB_NAME}}:v1.{{BUILD_ID}} /opt/docker


docker build -t $JOB_NAME:v1.$BUILD_ID .

=============
cd /opt/docker
docker build -t {{JOB_NAME}}:v1.{{BUILD_ID}} /opt/docker


docker push mahmudulrm/{{JOB_NAME}}:v1.{{BUILD_ID}}

docker rmi {{JOB_NAME}}:v1.{{BUILD_ID}} mahmudulrm/{{JOB_NAME}}:v1.{{BUILD_ID}}


valaxy/$JOB_NAME:latest
=================

---
- hosts: doc
  become: true
  gather_facts: no
  tasks:
  - name: enter the dir
    shell: cd /opt/docker
  - name: build java_demo_project
    shell: docker build -t {{JOB_NAME}}:v1.{{BUILD_ID}} /opt/docker
  - name: add tag
    shell: docker tag {{JOB_NAME}}:v1.{{BUILD_ID}} mahmudulrm/{{JOB_NAME}}:v1.{{BUILD_ID}}
  - name: add tag latest
    shell: docker tag {{JOB_NAME}}:v1.{{BUILD_ID}} mahmudulrm/{{JOB_NAME}}:latest
  - name: push old in docker hub
    shell: docker push mahmudulrm/{{JOB_NAME}}:v1.{{BUILD_ID}}
  - name: push latest in docker hub
    shell: docker push mahmudulrm/{{JOB_NAME}}:latest
  - name: remove docker
    shell: docker rmi {{JOB_NAME}}:v1.{{BUILD_ID}} mahmudulrm/{{JOB_NAME}}:v1.{{BUILD_ID}} 
  - name: remove latest docker
    shell: docker rmi mahmudulrm/{{JOB_NAME}}:latest
	
	
============

















