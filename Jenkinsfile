pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/yosrhaddar3-gif/exam.git'  // <-- ton fork
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
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
}

