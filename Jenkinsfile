pipeline {
    agent any
    tools {
      Maven "3.9.6"  
    }

    stages {
   

         stage('example') {
            steps {
              tool 'Maven 3.9.6'
        }
         }

        stage('List Workspace') {
            steps {
                script {
                    // List workspace contents
                    sh 'ls -al ${WORKSPACE}'
                }
            }
        }

         stage('example1') {
            steps {
                script {
                   
                    sh 'Maven --version'
                }
            }
        }
    
      
    }


}
