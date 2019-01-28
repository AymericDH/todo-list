pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                withMaven(
                    maven: 'M3'
                    JDK: 'JDK8'
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