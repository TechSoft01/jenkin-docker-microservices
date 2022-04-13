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
	//agent { docker { image 'maven:3.6.3'} }

	environment {
		dockerHome = tool 'mydocker'
		mavenHome = tool 'mymaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}

	stages {
		stage('Build') {
			steps {
				sh 'mvn --version'
				sh 'docker version'
				echo "Build"
				echo "path - $PATH"
				echo "Build_Number - $env.BUILD_NUMBER"
				echo "Build_id - $env.BUILD_ID"
				echo "job_name - $env.JOB_NAME"
				echo "Build_tag - $env.JOB_NAME"
				echo "build_url - $env.BUILD_URL"
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
	