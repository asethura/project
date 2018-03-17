pipeline{
	agent any
	
	stages {
		stage('checkout'){
			steps{
				checkout scm
			}
		}
		stage ('Build') {
			def mvnHome = tool 'M3'  
        	//sh "echo 'shell scripts to build project...'"
			steps{
				     
				sh "mvn package"
			}
			
			
        	}
	}
}
