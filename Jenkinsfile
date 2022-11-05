pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
                sh 'git clone https://github.com/EidoB/requests.git'
            }
        }
        stage('Build') {
            steps {
                sh 'python3 http_e.py'
            }
        }
        stage('Test') {
            steps {
                sh 'python3 TestRest.py '
            }
        }
        stage('Build Docker Image') {
            steps {
                agent { dockerfile true }
            }
        }
    }
}
