pipeline {
    agent any
    
    stages {
        /*stage('Checkout') {
            steps {
                // Checkout source code from SCM
                git 'https://github.com/superdoo/mavencalling.git'
            }
        }
        */
        
        stage('Build') {
            steps {
                // Use Maven to build the project
                sh 'mvn clean install'
            }
        }
        
    }
}
