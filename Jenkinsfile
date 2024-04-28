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

       stages {
        stage('Build') {
            steps {
                // Define Maven version and tool installation
                tool 'Maven'
                
                // Use Maven to build the project
                sh 'mvn clean install'
            }
        }
        }  
    stage('SonarQube Analysis') {
    steps{
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=MichaelsScan -Dsonar.projectName='MichaelsScan'"
    }
  }
      }
}

 
 
        
