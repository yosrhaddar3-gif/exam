pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/yosrhaddar3-gif/exam.git'
            }
        }

        stage('Install dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run tests') {
            steps {
                sh 'npm test'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t todo-app .'
            }
        }
    }

    post {
        failure {
            echo "Erreur dans le pipeline "
        }
        success {
            echo "Pipeline exécuté avec succès "
        }
    }
}
