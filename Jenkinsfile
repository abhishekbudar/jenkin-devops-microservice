// Below is a Scripted Pipleine approach

// Declartive pipeline
pipeline {
	agent any
	stages {
		stage('Build'){
			steps {
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
	} post {
		always{
			echo 'I am awesome'
		}
		sucess {
			echo 'When sucessful'
		}
		failure{
			echo 'When fail'
		}
	}
		
}

	