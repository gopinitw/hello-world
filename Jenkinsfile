pipeline {
    agent any
    
	tools {
	  maven "mvn"
		jdk "java11"
       	}	
    environment{
            scannerHome = tool 'SonarQube'
            tag = "${BUILD_NUMBER}“
                         }
       stages{								
        stage('MVN package Build') {
            steps {
                sh 'mvn clean install'
            }
        }
       }
}
