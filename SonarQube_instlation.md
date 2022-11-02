<h1>SonarQube setup</h1>

cd /opt

mkdir sonar

cd sonar

sudo yum install wget unzip -y 

sudo wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.0.zip

java version should 11 

unzip sonarqube-8.0.zip

mv sonarqube-8.0.zip sonarqube

<h5> Create new user </h5>

useradd sonar

visudo 

find out root and add below line in next line 

sonar ALL=(ALL)   ALL

controle X to exit 

to reopen it nano /etc/sudoers

<h4>to change the  the use in sonar qube file </h4>

ls -l 

you should be in /opt/sonar/sonarqube

chown -R sonar:sonar /opt/sonar/sonarqube

chmod -R 775 /opt/sonar/sonarqube

<h4> change the user to run sonarqube </h4>

su - sonar 

cd /opt/sonar/sonarqube

ls 

cd bin 

ls 

cd linux-x86-64

ls 

./sonar.sh start

./sonar.sh status


<h3> your ec2 instance public ip :9090</h3>

![](pictures/security%20inbount.png)















