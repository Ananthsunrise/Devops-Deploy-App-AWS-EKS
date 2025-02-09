# Devops-Deploy-App-AWS-EKS

**Overview**

If developer make changes github repo, it will trigger jenkins CI job through pollSCM. 
In CI Job, jenkins pull code from github repo and build the alrtifacts and push artifacts to ansible server. In ansible server, ansible playbook will create docker image and push into dockerhub using artifacts.Then CD job will automatically trigger.
In CD, Ansible server playbook uses kebernetes manifest files to deploy resources on Boostrap server which contains eks cluster using jenkins.

In this repo I attached clear documentation to implement this project.
Application repo: https://github.com/Ashfaque-9x/register-app.git
