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
  
  
 /*    stage('Build') {
      steps {
        container('jx-base') {
          sh 'docker build -t dhanapodigiri/poclistener:2.0 .'
		  sh 'docker images'
	
        }

      }
    }
*/
	  
    stage('Push') {
		steps{
			script {
				container('jx-base') {
				//sh 'docker images'
				//	sh 'whoami'
				//	sh 'cat /home/jenkins/.docker/config.json'
					sh 'chown "root":"root" /home/jenkins/.docker/ -R'
					sh 'chmod g+rwx "/home/jenkins/.docker/" -R'
					sh 'echo "dhana1234" | docker login --username dhanapodigiri --password-stdin'
				//sh 'docker push dhanapodigiri/poclistener:2.0'	
		//	sh "docker push dhanapodigiri/poclistener:1.0"
				}
			
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
