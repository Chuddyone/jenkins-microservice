//scripted
//node {
	//stage('Build') {
		//echo "Build"
	//}
	//stage('Test') {
		//echo "Test"


	//}
	//stage('Integration Test') {
		//echo "Integration Test"
	//}
//}

//declarative

pipeline {
	agent any
	//agent {docker { image "node:13.8"}}
	stages {
		stage ("Build") {
			steps {
				//sh "node --version"
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"	
				echo "BUILD_ID - $env.BUILD_ID"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_URL - $env.BUILD_URL"

			}
		}
		stage ("Test") {
			steps {
				echo "Test"	
			}
		}
		stage ("Integration Test") {
			steps {	
				echo "Integration Test"
			}
		}	
	} 
	post {
		always {
			echo "I always run"
		}
		success {
			echo "I run when all is successful"
	    }
		failure {
			echo "I run when you fail"
		}	

	}
}