pipeline {
    agent any
    tools {
        maven '3.9.6'
    }
      stages{

          stage(example){
          steps{
              sh 'mvn --version'
               
          }
          }

       
    stage('SonarQube Analysis') {
    //def mvn = tool '3.9.6';
    //withSonarQubeEnv() {
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=MichaelsScan -Dsonar.projectName='MichaelsScan'"
    }
  }
      }
}  
 
        
