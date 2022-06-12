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
                 echo 'Testing..'
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
