@Library('my-global-shared-library') _
pipeline {
    agent any
    tools {
        maven '3.9.6'
    }
      stages{

         /* stage(example){
          steps{
              sh 'mvn --version'
            
          }
          }
          */

         /*stage('Build') {
            steps {
                // Define Maven version and tool installation
                tool '3.9.6'
                
                // Use Maven to build the project
                sh 'mvn clean install'
            }
        }
        */
       
/*stage('SonarQube Analysis') {
            steps {
                // Set up SonarQube environment
                withSonarQubeEnv('sonarqube-server') {
                    // Perform actions within the SonarQube environment
                    sh "mvn sonar:sonar"
                  
                }
            }
        
        }
        */
stage('SonarQube Analysis') {
            steps {
            echo "Starting SonarQ Analysis"
            script{
            echo 'GIT_BRANCH:' + env.GIT_BRANCH
            try{
            writeFile file: "${env.WORKSPACE}/sonar-project.properties", text: "sonar.projectKey=MichaelsScan\n" +
            			"sonar.projectName=MichaelsScan\n" +
            			"sonar.projectVersion=${env.JENKINS_LIBRARY_VERSION}\n" +
            			"sonar.exclusions=**/node_modules/**,**/.serverless/**\n" +
            			"sonar.branch.name=${env.GIT_BRANCH}\n" +
            			"sonar.sources=.\n"
            	   sh "cat ${WORKSPACE}/sonar-project.properties"
            	   
            	      withSonarQubeEnv('sonarqube-server') {
                    // Perform actions within the SonarQube environment
                withSonarQubeEnv('sonarqube-server'){
                    sh "${tool(sonarscanner-5.0)}/bin/sonar-scanner"
                }
                    //sh "mvn sonar:sonar"                 
                }
       	   
            } catch(Exception e) {
               echo "EPIC FAILURE. ERROR: ${e}"
               }
            	  
        }
            }
}
      }
}

 
 
        
