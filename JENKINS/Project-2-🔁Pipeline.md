## How to Wrire Pipeline 🔁-🔁-🔁
***********************************-

After Configaration of Plugins And tools  use hallo-word syntx to write better
and copy and peaste multiple times for mutiple stages 

### Buld Pipeline
1 . this is 1 st stage intigrate pipeline with git repo
___________________________________________________

    pipeline {
        agent any

        environment {
            SCANER_HOME = tool 'SonarQube Scaner'
        }
        
        
        stages {
            stage ('git checkout') {
                steps {
                    git branch : 'main',
                    url : ( ** copy and peaste the our source code repo by pipeline syntax under folling steps ** )
                               
--> go to pipeline syntax --> Sample step { select *^ "git:Git" }<br>
--> Repository URL: " your github url --> Branch : main/Master
--> Credentials : select Your credentilas 
    ---> GENRATE PIPELINE SCRIPT 
    ( copy and peaste in git checkout step )

2 . this is 2 nd stage to intigrate with SonarQube 
______________________________________________________

          stage ('sonar-qube analysis') {
              steps {
                  WithSonarQubeEnv : ( 'Sonar-Server')
                     $SCANER_HOME/bin/SonarQube Scaner \
                     -Dsonar.projectName=amazon-prime \
                     -Dsonar.projectkey=amazon-prime
                  

--> go to pipeline syntax --> Sample step { select *^ "WithSonarQubeENV:" }
     ---> GENRATE PIPELINE SCRIPT 
        ( copy and peaste in SonarQube analysis step )

                  
              
    
   
 
               


            
