pipeline {
    agent any

    stages {
        stage('Clonar Repositório') {
            steps {
                // Clonar o repositório Git
                git url: 'https://github.com/FeMarquesSilva/TDE-DevOps', branch: 'main'
            }
        }

        stage('Instalar Dependências') {
            steps {
                // Criar ambiente virtual e instalar dependências
                sh '''
                    python3 -m venv venv
                    source venv/bin/activate
                    pip install -r requirements.txt
                '''
            }
        }

        stage('Executar Script') {
            steps {
                // Ativar o ambiente virtual e executar o script
                sh '''
                    source venv/bin/activate
                    ./automatizador.sh
                '''
            }
        }
    }
}

