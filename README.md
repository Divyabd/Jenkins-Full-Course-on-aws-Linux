# Jenkins-Full-Course-on-aws-Linux
Full steps of Jenkins On aws Linux 

<h1>  Create ec2 instance </h1>

<h2>  Instalation of Java on ec2 </h2>
Step 1. To install Java 11 on Amazon Linux 2, run:

sudo amazon-linux-extras install java-openjdk11
Step 2. Verify the installation.

java -version
Step 3. If you have multi-java environment, and you want to switch the java version, run:

alternatives --config java


<h2>  to switch to root user  </h2>
Become root using “sudo su -” command.


<h2> To install Jenkins  </h2>

  sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
  sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
 yum install fontconfig java-11-openjdk
  yum install jenkins
  
  
  

  
  
  
  Else follow below Doc 
     https://pkg.jenkins.io/redhat-stable/


  sudo service start jenkins 
  
then go to the  google copy public ip thn start 8080




    
    

