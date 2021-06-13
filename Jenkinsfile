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
		stage('Change Dir') {
			steps {
				echo '================================================++++'
				bat 'cd'
    				dir('target') {
      					bat 'cd'
   				 }
    				bat 'cd'
				echo '================================================++++'
			}
		}
		stage('Run') {
			steps {
				bat 'java -jar SpringBootDataRestDemo-1.0.jar'
			}
		}
		
	}
}
