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
    }
}
