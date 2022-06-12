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
                gradlew build -PARTIFACT_NAME="${ARTIFACT_NAME}"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}