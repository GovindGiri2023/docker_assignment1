pipeline{
	agent any
	stages{
		stage("Cleaning workspace"){
			steps{
				cleanWs ()
			}

		}
		stage("Checkout scp"){
			steps{
				checkout scm
			}
        }

        stage("Creating container"){
        	steps{
        		docker run --p 80:80 --name httpd_${GIT_BRANCH} httpd
        	}

        }
	}
	
}
