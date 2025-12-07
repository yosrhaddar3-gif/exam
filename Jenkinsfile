pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/yosrhaddar3-gif/exam.git' // ton fork
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'  // ou 'sh' si ton agent est Linux
            }
        }

        stage('Run Tests') {
            steps {
                bat 'npm test'     // ou 'sh' si Linux
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t todo-app .'  // ou 'sh' si Linux
            }
        }
    }
}




