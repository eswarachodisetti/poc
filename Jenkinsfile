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
     stage('Build') {
      steps {
        container('jx-base') {
       //   sh 'docker build -t dhanapodigiri/poclistener:2.0 .'
	//	  sh 'docker images'
	sh 'docker push dhanapodigiri/poclistener:2.0'
        }

      }
    }
 /* 
 stage('Validate Environment') {
      steps {
        container('jx-base') {
          dir('poclistener') {
               sh 'jx step helm apply --name poclistener'
                 sh 'jx step helm install --name=poclistener poclistener'       
       }
        }

      }
    }
	
*/
	
  }
}
