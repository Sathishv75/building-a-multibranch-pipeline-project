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
                sh './jenkins/scripts/test.sh'
            }
        } 
    }
}
