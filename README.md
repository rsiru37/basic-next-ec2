## The Steps followed in the Deployment
1. 2 Google Cloud Machines have been started one for Development & one for Production(The main Branch is for Prod & dev branch is for Dev Environment)
2. Github Workflow has been written for both the branched deploy_dev & deploy_prod. deploy_dev will only run when something has been pushed to the Dev Branch and deploy_prod will only run when something has been commited to the Main Branch
3. The respective private keys of both the ssh's of the Machines, have been added to the secrets of the github and workflow has been written to ssh into the Respective machines and run the latest github code of the respective branch(Condition is github code is already cloned into the machines)
4. While sshing into the machine, we also have to add ssh to the known_hosts file, b'coz we cannot type yes/no as github actions machine is a non-interactive environment.
5. rajsiruvani.in domain also has been mapped the dns records accordingly.
6. stagingdevops.rajsiruvani.in for the Dev Branch mapped to the external IP Address of the Google Cloud Virtual Machine
7. devops.rajsiruvani.in for the Main Branch mapped to the external IP Address of the Google Cloud Virtual Machine
