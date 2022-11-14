<h1>Terraform Installation on linuc ec2 and setup in jenkins tool </h1>

<h2>Installation of terraform on linux ec2</h2>

sudo su -

cd /opt

Follow below steps  / Link (https://developer.hashicorp.com/terraform/downloads)

sudo yum install -y yum-utils

sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/AmazonLinux/hashicorp.repo

sudo yum -y install terraform

To confirm terraform is installed run below command 

terraform -version 


