pipeline {
  agent any
   stages {
     stage('Build') {
     steps {
              sh 'docker build -t swmiwaghmare/jenkins:2.101 .'
            }
     }
       stage('Push to dockerhub') {
        agent any
         steps {
               withCredentials([usernamePassword(credentialsId: 'dockerHub', passwordVariable: 'dockerHubPassword', usernameVariable: 'dockerHubUser')]) {
          sh "docker login -u ${env.dockerHubUser} -p ${env.dockerHubPassword}"
          sh 'docker push swamiwaghmare/jenkins:2.101'
   
            }
        }
   }
 }
}

