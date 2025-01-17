# Creation of Kubernetes Cluster using kubeadm  
<a name="readme-top"></a>  

<!-- ABOUT THE PROJECT -->
## About The Project  
This repository is used as a part of bigger project and it is a second step and prerequisuite for step 3:
  

| Step              | Link                                                                                          | Description                                             |
|-------------------|-----------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Prerequisite step | [JenkinsCreator](https://github.com/jkb91jkb91/JenkinsCreator)                                | Creates Jenkins instance with jobs                      |
| Current step      | [Jenkins_KubeStarter](https://github.com/jkb91jkb91/Jenkins_KubeStarter)                      |                                                         |
| Next step         | [KubeServices](https://github.com/jkb91jkb91/KubeServices)                                    | Creates Kubernetes services                             |

Code from this repository is meant to deploy kubernetes cluster on EC2 intances    

This repository contains files related to IaC  
-terraform  
-ansible  

additional files:  
  -bashrc  
  -prepare_for_ansible.sh (to get IP and SSH KEY on local machine) 

<!-- TECHNOLOGIES -->
## Technologies

Technologies:
* ![AWS EC2](https://img.shields.io/badge/AWS%20EC2-232F3E?style=for-the-badge&logo=amazon%20aws&logoColor=white)
* ![Terraform](https://img.shields.io/badge/Terraform-623CE4?style=for-the-badge&logo=terraform&logoColor=white)
* ![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=for-the-badge&logo=ansible&logoColor=white)

<!-- DETAILED DESCRIPTION -->
## Detailed description

CODE FROM THIS REPO WILL BE TRIGGERED BY THIS JOBS (prerequisuite >>  https://github.com/jkb91jkb91/JenkinsCreator)  
Prerequisuite step will create for us JENKINS instance and bootstrap it with such jobs:  

JOB1 = A_terraform_stack_create.json  
JOB2 = B_ansible_stack_create.json  
JOB3 = C_ansible_stack_delete.json  
JOB4 = D_terraform_stack_delete.json  

   

STEP CREATION
To create the whole stack do:  
manual trigger ONLY JOB1: (JOB1 = A_terraform_stack_create.json >--automatically triggered-> JOB2 = B_ansible_stack_create.json)  

STEP REMOVING
To delete the whole stack do:  
manual trigger ONLY JOB3: (JOB3 = C_ansible_stack_delete.json   >--automatically triggered-> JOB4 D_terraform_stack_delete.json)  

<!-- RESULT -->
## Result

STEP CREATION RESULT = Created kubeadm kubernetes cluster with master and worker nodes being deployed on EC2 AWS instances  
STEP REMOVING RESULT = Removing whole stack from AWS  

<!-- AUTHOR -->
## Author
Email: jakub.g26101991@gmail.com


<p align="right">(<a href="#readme-top">back to top</a>)</p>
