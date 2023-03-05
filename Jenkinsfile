//Scripted
node {
	stage('Build') {
		
		echo "Build"
	}
	stage('Test') {
		echo "Test"
	}
	stage("Integration Test") {
		echo "Test"
	}
}


//Declarative
pipeline{
	agent any
	//agent { docker{image 'maven:3.6.3'} }
	stages {
		stage("Build"){
			steps{
				//sh "mvn --version"
				echo "Build"
				echo "$PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
			}
		}

		stage("Test"){
			steps{
				echo "Test"
			}
		}

		stage("Integration Test"){
			steps{
				echo "Integration Test"
			}
		}
	}

	post{
		always{
			echo "I'm awesome. I run always"
		}
		success{
			echo "I run when successful"
		}
		failure{
			echo "I run when I fail"
		}
	}
}