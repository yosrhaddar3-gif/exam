pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/yosrhaddar3-gif/exam.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }
        stage('Run Tests') {
            steps {
                bat 'npm test'
            }
        }
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t todo-app .'
            }
        }
        stage('Test Pipeline') {
            steps {
                echo 'Pipeline Windows prêt pour examen'
            }
        }
    }
}







