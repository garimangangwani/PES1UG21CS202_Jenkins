pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Add build steps here
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                // Add test steps here
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                // Add deploy steps here
                echo 'Deploying...'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}