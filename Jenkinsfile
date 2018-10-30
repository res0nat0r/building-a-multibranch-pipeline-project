pipeline {
    agent {
        docker {
            image 'node:6-alpine'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'pwd'
                sh 'id'
                sh 'hostname'
                sh 'ls -l'
                sh 'echo STEF > /tmp/stef'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}