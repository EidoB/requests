pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
                echo 'git'
            }
        }
        stage('Build') {
            steps {
                sh 'python http_e.py'
            }
        }
        stage('Test') {
            steps {
                sh 'python TestRest.py '
            }
        }
    }
}