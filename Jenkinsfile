pipeline {
    agent any

    stages {
        stage('Clonar Repositório') {
            steps {
                // Clonar o repositório Git
                git url: 'https://github.com/FeMarquesSilva/TDE-DevOps', branch: 'main'
            }
        }

        stage('Executar Script') {
            steps {
                // Executar o script .sh
                sh 'automatizador.sh'
            }
        }
    }
}
