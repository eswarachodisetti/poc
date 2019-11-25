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
					sh 'whoami'
					sh 'cd /home && ls -lart'
				//	sh 'sudo chown "root":"root" /home/"root"/.docker -R'
				//	sh 'sudo chmod g+rwx "/home/root/.docker" -R'
				//	sh 'echo "dhana1234" | docker login --username dhanapodigiri --password-stdin'
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
