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
			steps{
        			sh "${mvnHome}/bin/mvn clean install"
				//sh 'echo $PATH'
				
			}
			
        	}
	}
}
