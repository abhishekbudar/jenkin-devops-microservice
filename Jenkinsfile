// Below is a Scripted Pipleine approach

// Declartive pipeline
pipeline {
	agent any
	//agent { docker {image 'maven:3.6.3'}}

	environment {
        dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
    }
	stages {
		stage('Checkout'){
			steps {
				
				sh "mvn --version"
				sh "docker version"
				echo "Build"
			
			}
		}
		stage ('Compile'){
			steps {
				sh "mvn clean compile"
			}

		}
		stage('Test'){
			steps {
				sh "mvn Test"
			}
		}
		stage('IntegrationTest'){
			steps {
				sh "mvn failsafe:integration-test failsafe:verify"
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

	