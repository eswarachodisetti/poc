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
      //   sh 'jx step helm release eswarachodisetti_pkstest1_master'
//             sh 'jx step helm package eswarachodisetti_pkstest1_master'
       //   sh 'jx step create version pr -k charts -n eswarachodisetti_pkstest1_master-1.0.0.tgz'
        //    sh 'jx step helm install -n eswarachodisetti_pkstest1_master helm'
     sh 'jx step helm install --name poc' 
       }


      }
    }
  }
}
