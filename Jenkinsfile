pipeline {
    agent any

    stages {
	stage('SCM Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build & Test') {
		
				
            			steps {
                			bat "gradlew.bat build -PARTIFACT_NAME=${ARTIFACT_NAME} -PBUILD_VERSION=${BUILD_VERSION}"
            			}
        		
        		
            			steps {
					echo 'Unit Test'
            			}
        		
		
	}
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
