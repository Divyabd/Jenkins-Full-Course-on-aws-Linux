<h1>How to Install Artifactory in Ec2 Linux System and Configuration with the Jenkins </h1>

<h3>Pre-requisites</h3>

You need t2.medium instance or large t2.micro wont work  and 

Open port 8081 and 8082 in security group 

You need java to be installed 

cd opt 

cd jfrog

wget https://jfrog.bintray.com/artifactory/jfrog-artifactory-oss-6.9.6.zip

unzip jfrog-artifactory-oss-6.9.6.zip

ls 

cd jfrog-artifactory-oss-6.9.6

cd bin 

./artifactory.sh start


After start access jenkins using Publicip:8081

setup password -> skip(configure proxy server)-> Choose maven -> Finish it up 


<h3> Jenkins configuration with Jfrog </h3>
 

Open jenkins -> Manage Jenkins -> Manage plugins -> Install  Artifactory plugin -> install without restart 

Manage jenkins -> configure system -> jfrog -> give instance id (name) ->  give server link where jfrog running -> give username and password (before to that create new user in jfron under admin section and give admin privilage access ) test the connection -> save and apply 



NOTE::::::::::: (if test failed , click on advanced option and check for the artifact and sistribution atleast artifcatory should success)


Create free style job ->Build Environment->Maven3-Artifactory Integration(Do select release and snapshot) -> Build Steps ->Invoke Artifactory Maven 3
->  Maven/pom.xml -> clean install package 

 Run the build and check the release 
-
 

