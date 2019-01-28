pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo "Build phase"
            }
        }
        stage('Test') {
            steps {
                echo "Test phase"
            }
        }
    }
}