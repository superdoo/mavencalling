pipeline {
    agent any

    stages {
        stage('List Workspace') {
            steps {
                script {
                    // List workspace contents
                    sh 'ls -al ${WORKSPACE}'
                }
            }
        }
    
        stage('Install Maven') {
            steps {
                // Install Maven using the 'Maven' tool defined in Jenkins
                tool 'Maven'
            }
        }
    }


}
