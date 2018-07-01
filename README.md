# bb-project
## Skeleton:
Basic - - OK 
 - Create Vagrantfile for the test node - OK

 Kuberntes - - OK 
 - Create kubernetes role - OK 
 - Create kubernetes playbook - OK 
 - Create common role - OK 
    - Add dependencies -  docker - OK 

 Nginx   
 - Create nginx deployment files on kubebernetes -OK
 - Nginx playbook - OK
    - Create configmap - OK
    - Create index.html on configmap - OK
    - Run kubenernetes yaml for nginx - OK

Tomcat - OK
  - Create dockerfile for tomcat container
        - jdk8 based - OK
        - Download sample from - https://tomcat.apache.org/tomcat-8.0-doc/appdev/sample/ - OK
        - Build image - OK
  - Create tomcat deployment file on kubernetes - OK
  - Tomcat playbook - OK
    - Build container - OK
    - Run kubernetes yaml for tomcat - OK

Jenkins
   - Run a jenkins receipt to install jenkins in a kubernetes
   - Create a job remotely

Documentation
  - README
  - Requisites - OK
  - Comments on playbooks
  - Curls at the end
    - nginx
    - tomcat
  - Print jenkins url

## Requisites:
ansible 2.5 or later
Vagrant 2.1 or later
Virtualbox 5.2 or later
2 VCPUs
4Gb of Ram



## Running:
 $ vagrant up

Test Nginx:
  $ curl 192.168.56.11:31514

Test Tomcat:
  $ curl 192.168.56.11:31515/sample/

