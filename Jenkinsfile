// Below is a Scripted Pipleine approach

// Declartive pipeline
pipeline {
	//agent any
	agent { docker {image 'maven:3.6.3'}}
	stages {
		stage('Build'){
			steps {
				
				sh "mvn --version"
				echo "Build"
			}
		}
		stage('Test'){
			steps {
				echo "Test"
			}
		}
		stage('IntegrationTest'){
			steps {
				echo "Ingtegration Test"
			}
		}
	} 
	post {
		always{
			echo 'I am awesome, I know Jenkins'
		}
		success {
			echo 'When sucessful'
		}
		failure{
			echo 'When fail'
		}
	}
		
}

	