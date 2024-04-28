pipeline {
    agent any
    tools {
        maven '3.9.6'
    }
      stages{

          stage(example){
          steps{
              sh 'mvn --version'
            //this is bullshit  
          }
          }

         stage('Build') {
            steps {
                // Define Maven version and tool installation
                tool '3.9.6'
                
                // Use Maven to build the project
                sh 'mvn clean install'
            }
        }
       
    stage('SonarQube Analysis') {
    steps{
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=MichaelsScan -Dsonar.projectName='MichaelsScan'"
    }
  }
      }
}

 
 
        
