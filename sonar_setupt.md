<h2>After sonar successfully raned follow the below steps</h2>

Login to sonarqube (bydefault username and password is admin)

Change the  password 

Create new project 

Generate the token 

Copy the tocken somewhere else 

Goto Jenkins ->Manage jenkins-> Manage Credentials -> add credential -> add secret text 

Goto Jenkins -> Manage jenkins -> manage plugin -> sonarqube scanner

Mange Jenkins -> configure system ->check on enviroment variable under sonarqube-> give name -> public ip:9000(where is your sonarqube is running)-> select the credential

Manage jenkins -> Global tool configuration ->  sonarqube scaner -> give name -> save 

Manage jenkins -> tool configuration ->  Maven3 -> give name -> slect apachee->save


Create free style job -> Git link -> check the box  prepare sonarqube env ( Dont add any credential) -> Build step -> Invoke top-level Maven targets -. Maven3 -> clean install sonar:sonar -> Maven/pom.xml Save and build 



