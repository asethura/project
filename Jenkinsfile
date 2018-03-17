pipeline{
	agent any
	tools {
   		maven 'Maven 3.3.9'
  	}
	stages {
		stage('checkout'){
			steps{
				checkout scm
			}
		}
		stage ('Build') {
        	//sh "echo 'shell scripts to build project...'"
			steps{
				sh "mvn package"
			}
			
			
        	}
	}
}
