pipeline {
    agent any

    stages {
        stage('Clonar Repositório') {
            steps {
                git url: 'https://github.com/FeMarquesSilva/TDE-DevOps', branch: 'main'
            }
        }

        stage('Instalar Dependências') {
            steps {
                sh '''
                    python3 -m venv venv
                    . venv/bin/activate
                    pip install -r requirements.txt
                '''
            }
        }

        stage('Executar Script') {
            steps {
                sh '''
                    . venv/bin/activate
                    ./automatizador.sh
                '''
            }
        }
    }
}

