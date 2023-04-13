pipeline {
    	agent any
	tools {
		maven 'MAVEN_HOME'
		jdk 'JAVA_HOME'
	}
	options {
		buildDiscarder(logRotator(numToKeepStr: '5'))
	}

    	stages{
        	stage('Scan') {
            	steps{
                		withSonarQubeEnv(installationName: 'sq1') {
					sh "mvn clean verify"
				}
           		 }
      	 }
    	}
}
