pipeline {
    agent any
    
	tools {
	  maven "mvn"
		jdk "java11"
       	}	
       stages{								
        stage('MVN package Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('jacoco report coverage'){
            steps{
                jacoco()
                }
               }

       }
}
