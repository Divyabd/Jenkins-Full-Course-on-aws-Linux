<h1>SonarQube setup</h1>

cd /opt

mkdir sonar

cd sonar

sudo yum install wget unzip -y 

sudo wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.0.zip

java version should 11 ( cmd : java --version) ( command to install java : sudo dnf install java-11-amazon-corretto -y)

unzip sonarqube-8.0.zip

mv sonarqube-8.0 sonarqube

<h5> Create new user </h5>

useradd sonar

visudo 

find out root and add below line in next line 

sonar ALL=(ALL)   ALL

controle X to exit  or esc :wq

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


<h3> your ec2 instance public ip :9000</h3>


NOTE : BY DEFAULT SONARQUBE USERNAME AND PASSWORD IS admin ,admin login and change the password

<h5>Make sure your SG have below shown Inbound rules </h5>

![Make sure youe SG have below shown Inbound rules](pictures/security%20inbound.png?raw=true "Make sure youe SG have below shown Inbound rules")















