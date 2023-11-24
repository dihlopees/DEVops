pipeline {
    agent any
    stages {
        stage('Instalar Dependências') {
            steps {
                sh '''
                docker-compose up -d
                '''
            }
        }
        
        stage('Executar Testes') {
            steps {
                sh '''
                echo 'Executando npm test: '
                npm test
                echo 'Executando testes com cypress no comando npm test:ci: '
                npm run test:ci
                echo 'Executando teste end to end com cypress no comando npm test:e2e: '
                npm run test:e2e
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
