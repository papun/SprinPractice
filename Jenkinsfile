pipeline {
	agent any
	stages {
		stage('Echo') {
			steps {
				echo 'Hi, this is Papun'
			}
		}
		stage('Confirm') {
			steps {
				input('Do you want to proceed')
			}
		}
		
		stage('Clone') {
			steps {
				git branch: 'main', credentialsId: 'SpringGitHUb', url: 'https://github.com/papun/SprinPractice.git'
			}
		}
		stage('Build') {
			steps {
				sh 'mvn clean package'
			}
		}
		stage('Run') {
			steps {
				sh 'java -jar SpringBootDataRestDemo-1.0.jar'
			}
		}
	}
}
