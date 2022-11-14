<h1>Terraform Installation on linuc ec2 and setup in jenkins tool </h1>

<h2>Installation of terraform on linux ec2</h2>

Create iam role to run terraform via linux

Iam -> role -> create new role -> aws service -> ec2 -> administration full access -> tags -> name -> create 

once iam role creation done attach that role to ec2 instance where jenkins are running 

select ec2 instance -> action -> security -> Modify iam role -> select newly created role 

sudo su -

cd /opt

Follow below steps  / Link (https://developer.hashicorp.com/terraform/downloads)

sudo yum install -y yum-utils

sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/AmazonLinux/hashicorp.repo

sudo yum -y install terraform

To confirm terraform is installed run below command 

terraform -version 

to know terraform path run the below command 

whereis terraform


<h3>Jenkins terraform integration </h3>

Open jenkins -> Manage Jenkins -> Manage plugins -> available plugins -> Terraform -> Install without restart

Open jenkins -> Manage Jenkins -> Global tool Configuration -> Terraform -> give name and install it -> save 

Create new item -> name -> free style job -> select source code management and give git url where terraform code resides -> In Build Environment -> terraform -> Build step -> executable shell -> terraform -version  -> save and run the build



