pipeline{
	agent any
	def mvnHome = tool 'M3'  
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
