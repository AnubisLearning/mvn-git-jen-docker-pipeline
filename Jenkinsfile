pipeline{
	agent any
	
	stages{
		stage('Compiler'){
			steps{
			withMaven(maaven: '3_1_2'){
			sh 'mvn clean compile'}
			}
		}
		stage('Testing'){
			steps{
			withMaven(maaven: '3_1_2'){
			sh 'mvn test'}
			}
		}
		stage('Create WAR'){
			steps{
			withMaven(maaven: '3_1_2'){
			sh 'mvn install'}
			}
		stage('Copy WAR'){
			steps{
			sh 'cp /target/myFirstWebApplication.war /var/lib/jenkins/workspace/jen_aws/myFirstWebApplication.war'}
			}
		}
	
	}
}
