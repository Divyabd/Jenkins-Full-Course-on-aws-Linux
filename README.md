# Jenkins-Full-Course-On-AWS-Linux

Full steps of Jenkins On AWS Linux 

<img alighn="right" src="https://github.com/Divyabd/Jenkins-Full-Course-on-aws-Linux/blob/master/pictures/jenkins%20linuc%20ec2.jpg" alt="awslinexjenkins" width="700" length="900">

<h1>  Create LINUX ec2 instance </h1>

<h2> To install Jenkins  </h2>


  Follow the Below Link ( Official Document)  : https://www.jenkins.io/doc/tutorials/tutorial-for-installing-jenkins-on-AWS/
  
      (OR )

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
   
   
save and apply,  build the job  


<h2> MAVEN INSTALATION AND CONFIGURATION</h2>

Link : https://maven.apache.org/download.cgi?Preferred=ftp://ftp.osuosl.org/pub/apache/

 Copy Binary tar.gz archive Link 
  
  https://dlcdn.apache.org/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.tar.gz
  
  In you Linux system  execute below commands
  
  cd /opt
  
  mkdir maven 
  
  cd maven 
  
  wget https://dlcdn.apache.org/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.tar.gz
  
  tar -xvzf apache-maven-3.8.6-bin.tar.gz
  
  <h6>INSTALATION DNE </h6>
  
  <h5> to set up the path </h5>
  
  cd apache-maven-3.8.6-bin
  
  run <h4>pwd</h4> command to find path where maven installed copy the path run below command
  
  cd /root 
  
  vi .bash_profile
  
  Hit I in key board 
  
  M2_HOME=/opt/maven/apache-maven-3.8.6-bin
 
 M2=$M2_HOME/bin
  
 PATH=$PATH:$JAVA_HOME:$M2_HOME:$M2:$HOME/bin
 
 hit ESC thn type :wq
 
  Relogin to instance 
 
 
 <h4>To  setup maven in jenkins </h4>
 
 Manage Jenkins-> manage plugin->available -> maven invoke , Maven Integration-> instal without restart 
 
 Manage Jenkins -> global tool configuration -> maven -> add Maven -> name = Maven , Uncheck install automaticaly box , -> MAVEN _HOME=/opt/maven/apache-maven-3.8.6-bin
 
 
 <h3>Install git on ec2 instance </h3>
 
 yum install git -y
 
  <h4>To  setup git in jenkins </h4>
  
  Manage Jenkins -> Manage plugins -> available plugins -> Git -> install without restart
  
   Manage Jenkins -> global tool configuration -> Git -> nothing to change 
  
  
  

   
   











    
    

