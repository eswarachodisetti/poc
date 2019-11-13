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
          dir('env') {

               sh 'jx step helm apply --name env'
            sh 'jx step helm charts'
       //    sh 'jx step helm install --name=poc http://jenkins-x-chartmuseum:8080/env'
        //  sleep 120
       
       }
        }

      }
    }
  }
}
