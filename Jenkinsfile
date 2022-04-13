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
	//agent any
	agent { docker { image 'maven:3.6.3'} }
	stages {
		stage('Build') {
			steps {
				sh 'mvn --version'
				echo "Build"
			}
		}
		stage('Test') {
			steps {
				echo "Test"
			}
		}
		stage('integration test') {
			steps {
				echo "integration Test"
		    }
		} 
	}	
		
		post {
			always{
				echo "i always run"
			}
			success {
				echo "i execute successfully"
			}
			failure{
				echo "i run failure"
			}
		}
     
}
	