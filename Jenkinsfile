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
                sh './gradlew.bat build'
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
