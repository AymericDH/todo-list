pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                mvn clean compile
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