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
		stage('Display') {
			steps {
				bat 'cd'
			}
		}
		stage('docker build') {
			steps {
				bat 'docker build -t myapp:v1 .'
				
				bat 'docker run -d -p 8081:8081 myapp:v1'
			}
		}
		stage('Run') {
			steps {
				echo 'finished/////'
			}
		}
		
	}
}
