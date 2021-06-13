pipeline {
	agent any
	stages {
		stage('Clone') {
			steps {
				echo 'Hi, this is Papun'
			}
		}
		
		stage('Two') {
			steps {
				git branch: 'main', credentialsId: 'SpringGitHUb', url: 'https://github.com/papun/SprinPractice.git'
			}
		}
	}
}
