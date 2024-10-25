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
                // Instalar dependências do Python
                sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Executar Script') {
            steps {
                // Dar permissão de execução ao script, se necessário
                sh 'chmod +x automatizador.sh'
                
                // Executar o script automatizador.sh
                sh './automatizador.sh'
            }
        }
    }
}
