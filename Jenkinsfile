pipeline {
    agent any

    stages {
	stage('Info'){
		steps {
			echo "${BUILD_NUMBER}"
			echo "${BUILD_ID}"
			echo "${BUILD_URL}"
			echo "${NODE_NAME}"
			echo "${JOB_NAME}"
			echo "${BUILD_TAG}"
			echo "${JENKINS_URL}"
			echo "${EXECUTOR_NUMBER}"
			echo "${JAVA_HOME}"
			echo "${WORKSPACE}"
			echo "${GIT_COMMIT}"
			echo "${GIT_URL}"
			echo "${GIT_BRANCH}"
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
