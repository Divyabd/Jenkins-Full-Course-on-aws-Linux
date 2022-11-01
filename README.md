# Jenkins-Full-Course-on-AWS-Linux
Full steps of Jenkins On AWS Linux 

<h1>  Create LINUX ec2 instance </h1>

<h2>  Instalation of Java on ec2 </h2>

Step 1. To install Java 11 on Amazon Linux 2, 

run:
sudo amazon-linux-extras install java-openjdk11

Step 2. Verify the installation.

java -version

Step 3. If you have a multi-java environment, and you want to switch the java version, run:

alternatives --config java


<h2>  to switch to root user  </h2>

Become root using “sudo su -” command.

<h2>To set path for JAVA</h2>

You can use any step to get your java installed path 

Step 1 : sudo find /usr/ -name *jdk

Step 2 :  java -XshowSettings:properties -version 2>&1 > /dev/null | grep 'java.home'

 Result : /user/lib/jvm/java_1.01.0(filename)
 
 NOTE:Copy the path 
 
 open .bash_profile using the below command 
 
 vi .bash_profile
 
 Once file is opened hit I on keyboard, in a new line enter the below line 
 
 JAVA_HOME= /user/lib/jvm/java_1.01.0(filename)
 
 Modify the path 
 
 BEFORE PATH 
  
  PATH=$HOME:$HOME/bin
  
  MODIFICATIONS NEED TO BE DONE LIKE 
  
  PATH=$HOME:$JAVA_HOME:$HOME/bin
  
  after all changes hit ESC then type :wq enter it will exit from vi editor 
  

<h2> To install Jenkins  </h2>

  sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
  
  sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
 
 yum install fontconfig java-11-openjdk
  
  yum install jenkins
  
 <h6>Else follow below Doc </h6>
     https://pkg.jenkins.io/redhat-stable/

<h5> TO START AND STOP JENKINS </h5>

sudo service jenkins start

sudo service jenkins stop
  
after jenkins start 
open the new tab and type your ec2 instance public ip:8080

<h3>Setting up java in Jenkins </h3>
  Open jenkins-> Manage Jenkins->Global tool Configuration->jdk->name=java , uncheck the install automatically box 
   JAVA_HONE =/user/lib/jvm/java_1.01.0(filename)
   
   save and apply  build the job 
   
   











    
    

