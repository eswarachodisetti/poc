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
  /*
  
     stage('Build') {
      steps {
        container('jx-base') {
          sh 'docker build -t dhanapodigiri/poclistener:5.0 .'
		  sh 'docker images'
	
        }

      }
    }

	  
    stage('Push') {
		steps{
			script {
				container('jx-base') {
				//sh 'docker images'
				//	sh 'whoami'
				//	sh 'cat /home/jenkins/.docker/config.json'
				//	sh 'chown -R "root":"root" /home/jenkins/.docker/*.*'
				//	sh 'chmod -R g+rwx "/home/jenkins/.docker/*.*"'
				//	sh 'echo "dhana1234" | docker login --username dhanapodigiri --password-stdin'
				//sh 'docker push dhanapodigiri/poclistener:2.0 --username dhanapodigiri --password=dhana1234'	
					sh 'mount -o remount,rw /home/jenkins/.docker'
				//	sh 'mount'
					sh 'scp ${WORKSPACE}/config.json /home/jenkins/.docker/'
					sh 'docker push dhanapodigiri/poclistener:5.0'	
		//	sh "docker push dhanapodigiri/poclistener:1.0 --username dhanapodigiri --password=dhana1234"
				}
			
			}
		}
	}
	     
	
	  
	*/  
  
 stage('Validate Environment') {
      steps {
        container('jx-base') {
          dir('poclistener') {
               sh 'jx step helm apply --name poclistener'
                   
       }
        }

      }
    }
	

	
  }
}
