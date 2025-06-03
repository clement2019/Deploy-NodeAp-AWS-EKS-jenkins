# project Outlook and workflow

- provisioing the myapp-server(jenkins) sitting on an EC2 instance created
- Accessibility to this Ec2 instance through port 8080 defined in SG
- the user me can only have access through SSH connection
- The provioning was done solely using terraform (IAC)

###  Workflow for this task using Terraform?
- VPC creation effected to start with
- Internet Gateway created while attaching it the VPC using a Route Table
- Public Subnet creation and associate it with the Route Table
- Security Group creation for firewall for the EC2 Instance
- Jenkins installation on the EC2 Instance done with script automation
- using an existing Key Pair to the Ec2 instance(myapp-server) created
- Making sure all works as specified

###  project Prerequisites
Installation and configuration of AWS CLI
Installation of Terraform


###  Run this to SSH into EC2
ssh -i devops_key2.pem amazon@public_ip

###  Use this to get the jenkins Admin password
sudo cat /var/lib/jenkins/secrets/initialAdminPassword

once jenkins is installed

###  Now change directory to infra from the project folder
cd infra
###  configure jenkins
install plugin node on jenkins
###  go to tools and add node inside node.js
now go to mamage jenkins
add credentials that the pipeline will use
### add Github credentials
username and password
Add Id:  GITHUB_CREDENTIALS
###  add dockerhub credentials
dockerhub id
dockkerhub username
dockerhubpassowrord as "secret test" in jenkins

add the name of kuberntestes cluster to deploy the application

  
