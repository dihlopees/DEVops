pipeline {
    agent any
    stages {
        stage('Instalar Dependências') {
            steps {
                sh '''
                docker-compose up -d
                node -v
                npm -v
                '''
            }
        }
        
        stage('Executar Testes') {
            steps {
                sh '''
                echo 'Executando npm test: '
                '''
            }
        }
    }
    
    post {
        always {
            sh '''
            echo 'Start no projeto NodeGoat, pipeline implementada pela aluna Ingrid Lopes R.A: 22.6980-1'
            npm start
            '''
        }
    }
}
