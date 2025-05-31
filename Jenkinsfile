pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('teste-jenkins')
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    docker.image('teste-jenkins').inside {
                        sh 'echo "Executando container teste-jenkins"'
                    }
                }
            }
        }
    }
}
