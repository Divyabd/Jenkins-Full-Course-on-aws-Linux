<h1> Jenkins and aws service connection</h1>

<h2> we are demostration How to deploy artifatcts to aws s3 bucket </h2>

Create iam role -> name -> aw service -> under that select ec2 -> add s3 full access 

open ec2 instnace -> select ec2 on which jenkins are ruuning -> actions -> security -> modify iam role -> choose one you have created -> save 

Create 1 s3 cuket in aws, any region 

jenkins -> Manage jenkins -> Manage plugins -> s3 publisher -> install without restart

jenkins -> Manage jenkins -> system configuration -> s3 publisher -> give the name -> click on iam role ( dont give access key and secrete key ) -> save 

Create Maven Jov -> give all maven info -> after build ->in post build action -> select publish artifatcs to s3 bucjet -> give workspace where .jar file is storing ->have a file formate -> give s3 bucket name and region -> if you want give additional info -> save -> build now 



