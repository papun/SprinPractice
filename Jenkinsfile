pipeline {
	agent any
	stages {		
		stage('Clone') {
			steps {
				git branch: 'main', credentialsId: 'SpringGitHUb', url: 'https://github.com/papun/SprinPractice.git'
			}
		}
		stage('Build') {
			steps {
				bat 'mvn clean package'
			}
		}
		stage('Run') {
			steps {
				bat 'java -jar target/SpringBootDataRestDemo-1.0.jar'
			}
		}
		
	}
}
