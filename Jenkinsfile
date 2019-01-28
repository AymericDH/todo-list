pipeline {
    agent any
    tools {
        maven 'M3'
        jdk 'JDK8'
    }
    stages {
        stage('Build') {
            steps {
                withMaven(
                    maven: 'M3',
                    mavenSettingsConfig: 'ArtifactoryConfig'
                ){
                    sh 'mvn clean compile'
                }
            }
        }
        stage('Test') {
            steps {
                withMaven(
                    maven: 'M3'
                ){
                    sh 'mvn test'
                }
            }               
        }
        stage('Install') {
            steps {
                withMaven(
                    maven: 'M3',
                    mavenSettingsConfig: 'ArtifactoryConfig'
                ){
                    sh 'mvn install -DskipTests=true'
                }
            }
        }
        stage('Deploy') {
            steps {
                withMaven(
                    maven: 'M3',
                    mavenSettingsConfig: 'ArtifactoryConfig'
                ){
                    sh 'mvn deploy -DskipTests=true'
                }
            }
        }
    }
}