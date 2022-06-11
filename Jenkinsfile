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
                gradele build
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