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
	//agent any
	agent {docker { image "redis"}}
	stages {
		stage ("Build") {
			steps {
				sh "redis --version"	
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