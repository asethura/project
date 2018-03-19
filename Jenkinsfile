pipeline{
	agent any
	environment {
        	MAVEN_HOME = tool('M3')
    	}
	stages {
		stage('checkout'){
			steps{
				checkout scm
			}
		}
		stage ('Build') {
			steps{
        			sh "${MAVEN_HOME}/bin/mvn clean install"
				//sh 'echo $PATH'
				
			}
			
        	}
		
		stage ('Test') {
			steps{
				sh "${MAVEN_HOME}/bin/mvn test surefire-report:report"
				publishHTML target: [
				    allowMissing: false,
				    alwaysLinkToLastBuild: false,
				    keepAll: true,
				    reportDir: 'coverage',
				    reportFiles: 'index.html',
				    reportName: 'RCov Report'
          					]
      				}
			}						
        }
				
}
