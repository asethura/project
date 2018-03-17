pipeline{
	agent any
	
	stages {
		stage('checkout'){
			steps{
				checkout scm
			}
		}
		stage ('Build') {
			
        	withMaven(
        	// Maven installation declared in the Jenkins "Global Tool Configuration"
        	maven: 'M3')
		sh "mvn clean install"	
			
        	}
	}
}
