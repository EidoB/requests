pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
                git https://github.com/EidoB/requests.git
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
