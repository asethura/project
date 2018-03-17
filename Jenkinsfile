pipeline{
	agent any
	
	stages {
		stage('checkout'){
			steps{
				checkout scm
			}
		}
		stage ('Build') {
			
        		sh "mvn clean install"	
			
        	}
	}
}
