pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '''
                docker info
                java --version
                docker compose version
                '''
            }
        }
    }
}