pipeline{
	agent any
	parameters{
		string(name: "PORT", description: "Please assign one port number to docker container:")
	}
	stages{
		stage("Cleaning workspace"){
			steps{
				cleanWs ()
			}

		}
		stage("Removing Runnint container"){
			steps{
				sh "sudo docker rm httpd_${GIT_BRANCH}"
			}
        	}

        	stage("Creating container"){
        		steps{
				sh "sudo docker run -dp ${PORT}:80 --name httpd1_${GIT_BRANCH} httpd"
        		}

        }
	}
	
}
