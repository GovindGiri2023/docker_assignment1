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
        		sh "docker run -dp 80:80 --name httpd_${GIT_BRANCH} httpd"
        	}

        }
	}
	
}
