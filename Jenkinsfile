pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                withMaven(
                    maven: 'M3'
                ){
                    sh 'mvn clean compile'
                }
            }
        }
        stage('Test') {
            steps {
                echo "Test phase"
            }
        }
    }
}