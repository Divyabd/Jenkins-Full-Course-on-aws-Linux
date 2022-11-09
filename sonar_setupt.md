<h2>After sonar successfully raned follow the below steps</h2>

Login to sonarqube (bydefault username and password is admin)

Change the  password 

Create new project 

Jenerate the tocken 

Copy the tocken somewhere else 

Goto Jenkins -> Manage Credentials -> add credential -> add secret text 

Mange Jenkins -> configure system ->check on enviroment variable under sonarqube-> give name -> public ip:9000(where is your sonarqube is running)-> select the credential

Manage jenkins -> tool configuration ->  sonarqube snaccer -> give name -> save 

