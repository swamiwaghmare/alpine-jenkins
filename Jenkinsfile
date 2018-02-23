pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t liatrio/new-alpine:2.101 .'
            }
        }
        stage('Push to dockerhub') {
            steps {
                sh 'docker push liatrio/new-alpine:2.101'
            }
        }
    }
}
