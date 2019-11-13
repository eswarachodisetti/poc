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

               sh 'jx step helm apply --name poclistener'
       //  sleep 120
           sh 'jx step helm install --name=poc poclistener'
        //       sh 'jx step helm apply'
        
       
       }
        }

      }
    }
  }
}
