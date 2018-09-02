pipeline{
	agent any
	
	stages{
		stage('Compiler'){
			steps{
			sh 'mvn clean compile'}
			
		}
		stage('Testing'){
			steps{
			sh 'mvn test'}
			
		}
		stage('Create WAR'){
			steps{
			sh 'mvn install'}
			
		}
		stage('Copy WAR'){
			steps{
			sh 'cp /target/myFirstWebApplication.war /var/lib/jenkins/workspace/jen_aws/myFirstWebApplication.war'}
		}
		
	
	}
}
