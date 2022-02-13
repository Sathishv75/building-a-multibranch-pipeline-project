pipeline {
    agent any
    environment {
        CI = 'true'
   }
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello world!"'
            }
        }
        stage('Test') {
            steps {
                sh 'whoami'
                sh './jenkins/scripts/test.sh'
            }
        }
        stage('Deliver for development') {
            when {
                branch 'development'
            }
            steps {
                sh './jenkins/scripts/deliver-for-development.sh'
                input message: 'Finished using the development web site? (Click "Proceed" to continue)'
            }
        }
    }
}
