pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Trigger the 'PES1UG21CS202-1' Jenkins job for building
                    build 'PES1UG21CS202-1'
                    // Compile the new_file.cpp using shell script
                    sh 'g++ -o new_file new_file.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run the executable of the compiled C++ file
                    sh './new_file'
                }
            }
        }

        stage('Deploy') {
            steps {
                // Add steps for deployment if needed
                echo 'Deploy'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
