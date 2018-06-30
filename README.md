# bb-project
## Skeleton
Basic - - OK 
 - Create Vagrantfile for the test node - OK

 Minikube - - OK 
 - Create minikube role - OK 
 - Create minikube playbook - OK 
 - Create common role - OK 
    - Add dependencies -  docker - OK 

 Nginx   
 - Create nginx deployment files on kubebernetes
 - Nginx playbook
    - Create folder for volume
    - Create index.html on volume folder
    - Run kubenernetes yaml for nginx

Tomcat
  - Create dockerfile for tomcat container
        - alpine jdk8 based
        - Download sample from - https://tomcat.apache.org/tomcat-8.0-doc/appdev/sample/
        - Use experimental parameters Java8 for JVM on kubernetes
        - Build image
  - Create tomcat deployment file on kubernetes
  - Tomcat playbook
    - Build container
    - Run kubernetes yaml for tomcat

Jenkins
   - Run a jenkins receipt to install jenkins in a minikube
   - Create a job remotely

Documentation
  - README
  - Requisites
  - Comments on playbooks
  - Curls at the end
    - nginx
    - tomcat
  - Print jenkins url
