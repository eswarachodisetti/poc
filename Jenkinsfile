pipeline {
  options {
    disableConcurrentBuilds()
  }
  agent {
    label "jenkins-jx-base"
  }
  environment {
    DEPLOY_NAMESPACE = "jx-staging"
  }
  stages {
    stage('Validate Environment') {
      steps {
        container('jx-base') {
          dir('poclistener') {

               sh 'jx step helm apply --name env'
       //  sleep 120
           sh 'jx step helm install --name=poc storage.googleapis.com/env'
        
       
       }
        }

      }
    }
  }
}
