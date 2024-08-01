# Creation of Kubernetes Cluster using kubeadm on AWS EC2 with the help of IaC: Terraform and Ansible  
<a name="readme-top"></a>  

<!-- ABOUT THE PROJECT -->
## About The Project  
This repository is used as a part of bigger project and it is triggered by JENKINS JOBS created as prerequsuite here:
https://github.com/jkb91jkb91/JenkinsCreator  

CODE FROM THIS REPO WILL BE TRIGGERED BY THIS JOBS  
JOB1 = A_terraform_stack_create.json  
JOB2 = B_ansible_stack_create.json  
JOB3 = C_ansible_stack_delete.json  
JOB4 = D_terraform_stack_delete.json  

This repository contains files related to IaC  
-terraform  
-ansible  
additional files:   
-bashrc file  
-prepare_for_ansible.sh (to get IP and SSH KEY on local machine)  
T
<!-- TECHNOLOGIES -->
## Technologies

Technologies used to create this site:
* ![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white)
* ![Groovy](https://img.shields.io/badge/Groovy-4298B8?style=for-the-badge&logo=apache%20groovy&logoColor=white)
* ![AWS EC2](https://img.shields.io/badge/AWS%20EC2-232F3E?style=for-the-badge&logo=amazon%20aws&logoColor=white)
* ![Route 53](https://img.shields.io/badge/Route%2053-232F3E?style=for-the-badge&logo=amazon%20route%2053&logoColor=white)
* ![Terraform](https://img.shields.io/badge/Terraform-623CE4?style=for-the-badge&logo=terraform&logoColor=white)
* ![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=for-the-badge&logo=ansible&logoColor=white)

<!-- DETAILED DESCRIPTION -->
## Detailed description
Jenkins Jobs uses this repo in their "steps"  
Jenkins with JOBS should be created as prerequisuite in this project:
https://github.com/jkb91jkb91/JenkinsCreator  

STEP CREATION
To create the whole stack do:  
manual trigger ONLY JOB1: (JOB1 = A_terraform_stack_create.json >--automatically triggered-> JOB2 = B_ansible_stack_create.json)  

STEP REMOVING
To delete the whole stack do:  
manual trigger ONLY JOB3: (JOB3 = C_ansible_stack_delete.json >--automatically triggered-> D_terraform_stack_delete.json)  

<!-- RESULT -->
## Result

STEP CREATION WILL RESULT WITH = Created kubeadm kubernetes cluster with master and worker nodes being deployed on EC2 AWS instances  
STEP REMOVING WILL RESULT WITH = Removing whole stack from AWS  

<!-- AUTHOR -->
## Author
Email: jakub.g26101991@gmail.com


<p align="right">(<a href="#readme-top">back to top</a>)</p>
