<h1>How to Install Artifactory in Ec2 Linux System</h1>

<h3>Pre-requisites</h3>

You need t2.medium instance or large te.micro wont work  and 

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

