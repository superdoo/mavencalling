pipeline {
    agent any
    tools {
      Maven 
    }

    stages {
        stage('List Workspace') {
            steps {
                script {
                    // List workspace contents
                    sh 'ls -al ${WORKSPACE}'
                }
            }
        }

         stage('example') {
            steps {
                script {
                   
                    sh 'Maven --version'
                }
            }
        }
    
      
    }


}
