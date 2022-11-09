
pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/EidoB/requests.git']]])
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
    }
    post {
        success{
           sh 'docker build -t hotipythontest .'
        }
    }
}
