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
         stage('Junit Test execution and report generation') {
             steps{
                 sh 'mvn test'
                  }
             post{
                 always{
                     junit '**/target/surefire-reports/TEST-*.xml'
                        }
                 }
            }


       }
}
