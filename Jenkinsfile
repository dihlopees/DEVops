pipeline {
    agent any
    stages {
        stage('Subindo com docker') {
            steps {
                sh '''
                docker-compose up -d
                '''
            }
        }

        stage('Instalar Dependências'){
            steps {
                sh '''
                npm install
                '''
            }
        }
        
        stage('Executar Testes') {
            steps {
                sh '''
                echo 'Executando npm test: '
                npm run test
                '''
            }
        }
    }
    
    post {
        always {
            sh '''
            echo 'Start no projeto NodeGoat, pipeline implementada pela aluna Ingrid Lopes R.A: 22.6980-1'
            '''
        }
    }
}
