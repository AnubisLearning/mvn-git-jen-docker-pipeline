pipeline{
	agent any
	
	stages{
		stage('Compiler'){
			steps{
			withMaven(maaven: '3.1.2'){
			sh 'mvn clean compile'}
			}
		}
		stage('Testing'){
			steps{
			withMaven(maaven: '3.1.2'){
			sh 'mvn test'}
			}
		}
		stage('Deployment'){
			steps{
			withMaven(maaven: '3.1.2'){
			sh 'mvn deploy'}
			}
		}
	
	}
}