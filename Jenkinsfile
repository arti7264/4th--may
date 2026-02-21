pipeline {
    agent { label 'maven' }   // run on agent node

    stages {
        stage('Build on Agent') {
            steps {
                sh 'hostname'
                sh 'mvn -version'
                sh 'mvn clean package'
            }
        }
    }
}
