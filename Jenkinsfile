pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    build 'PES1UG22CS223-1'
                    sh 'g++ main.cpp -o output'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './output'
                }
            }
        }

        stage('Deployy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
