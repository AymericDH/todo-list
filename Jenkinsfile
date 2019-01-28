pipeline {
    agent any
    tools {
        maven 'M3'
        jdk 'JDK8'
    }
    stages {
        stage('Build') {
            echo "Build phase"
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