//Scripted Pipeline
//node {
//	stage('Build') {
//		echo "Build"
//	}
//	stage('Test') {
//		echo "Test"
//	}
//	stage('Integration Test') {
//		echo "Test"
//	}
//}

//Declarative pipeline

pipeline {
	agent any
	stages {
		stage('Build') {
			step {
				echo "Build"
			}
		}
		stage('Test') {
			step {
				echo "Test"
			}
		}
		stage('integration test') {
			step {
				echo "integration Test"
		    }
		}
     }
}
	