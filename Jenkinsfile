pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES2UG22CS134-1 PES2UG22CS134-1.cpp' 
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES2UG22CS134-1'  
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment Step'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed. Check the logs for errors.'
        }
    }
}
