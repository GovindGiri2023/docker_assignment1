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
        			sh "sudo docker run -dp 80:80 --name httpd1 httpd"
        		}

        }
	}
	
}
