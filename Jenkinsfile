pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o pes2ug22cs134-1 pes2ug22cs134-1.cpp' 
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './pes2ug22cs134-1'  
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
