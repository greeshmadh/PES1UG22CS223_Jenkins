pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    build 'PES1UG22CS223-1'
                    sh 'g++ -wrongflag main.cpp -o output'
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

        stage('Deploy') {
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
