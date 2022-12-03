// Below is a Scripted Pipleine approach

// Declartive pipeline
pipeline {
	agent any
	//agent { docker {image 'maven:3.6.3'}}

	enviornment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage('Build'){
			steps {
				
				sh "mvn --version"
				sh "docker version"
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

	