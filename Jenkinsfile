pipeline {
    agent any

    stages {
		stage('pre-requisites') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                bat "gradlew.bat build -PARTIFACT_NAME=${ARTIFACT_NAME} -PBUILD_VERSION=${BUILD_VERSION}"
            }
        }
        stage('Test') {
            steps {
		echo "${ARTIFACT_NAME}"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
