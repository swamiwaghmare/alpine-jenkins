pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t new-Docker-image:0.1 .'
            }
        }
        stage('Push to dockerhub') {
	 agent any
         steps {
          withCredentials([usernamePassword(credentialsId: 'dockerHub', passwordVariable: 'dockerHubPassword', usernameVariable: 'dockerHubUser')]) {
          sh "docker login -u ${env.dockerHubUser} -p ${env.dockerHubPassword}"
          sh 'docker push swamiwaghmare/jenkins-alpine:2.101'		
          
            }
        }
    }
}
}
