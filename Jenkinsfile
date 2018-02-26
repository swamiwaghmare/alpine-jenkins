pipeline {
    agent any
     stages {
        stage('Build') {
            steps {
                sh 'docker build -t swamiwaghmare/jenkins-alpine:2.101 .'
            }
        }
        stage('Push to dockerhub') {
            steps {
                sh 'docker push swamiwaghmare/jenkins-alpine:2.101'
            }
        }
    }
}

