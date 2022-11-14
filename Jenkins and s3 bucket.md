<h1> Jenkins and aws service connection</h1>

<h2> we are demostration How to deploy artifatcts to aws s3 bucket </h2>

Create iam role -> name -> aw service -> under that select ec2 -> add permission s3 full access -> name it -> save 

open ec2 instnace -> select ec2 on which jenkins are ruuning -> actions -> security -> modify iam role -> choose one you have created -> save 

Create 1 s3 cuket in aws, any region 

jenkins -> Manage jenkins -> Manage plugins ->available plugins -> s3 publisher -> install without restart

jenkins -> Manage jenkins -> Configure System ->Amazon S3 profiles -> give the name -> click on Use iam role ( dont give access key and secrete key ) -> save 

Create Maven Job -> give all maven info -> after build ->in post build action -> select Publish artifacts to S3 Bucket -> give workspace where .jar file is storing ->have a file formate -> give s3 bucket name and region -> if you want give additional info -> save -> build now 



