pipeline {
    agent any

    stages {
	stage('Info'){
		steps {
			echo "BUILD_NUMBER=${BUILD_NUMBER}"
			echo "BUILD_ID=${BUILD_ID}"
			echo "BUILD_URL=${BUILD_URL}"
			echo "NODE_NAME=${NODE_NAME}"
			echo "JOB_NAME=${JOB_NAME}"
			echo "BUILD_TAG=${BUILD_TAG}"
			echo "JENKINS_URL=${JENKINS_URL}"
			echo "EXECUTOR_NUMBER=${EXECUTOR_NUMBER}"
			echo "JAVA_HOME=${JAVA_HOME}"
			echo "WORKSPACE=${WORKSPACE}"
			echo "GIT_COMMIT=${GIT_COMMIT}"
			echo "GIT_URL=${GIT_URL}"
			echo "GIT_BRANCH=${GIT_BRANCH}"
		}
	}
	stage('SCM Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
		steps {
			bat "gradlew.bat build -PARTIFACT_NAME=${ARTIFACT_NAME} -PBUILD_VERSION=${BUILD_VERSION}"
            	}
	}
	stage('Unit Test'){
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
