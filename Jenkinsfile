pipeline {
    agent {
        docker {
            image 'node:6-alpine'
#            args '-p 3000:3000 -p 5000:5000' 
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