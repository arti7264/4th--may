pipeline {
    agent any

    tools {
        maven 'maven'
    }

    stages {

        stage('Build') {
            steps {
                dir('devops-demo') {   // <-- folder containing pom.xml
                    sh 'mvn clean package'
                }
            }
        }

        stage('Archive Artifact') {
            steps {
                dir('devops-demo') {
                    archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
                }
            }
        }
    }
}
