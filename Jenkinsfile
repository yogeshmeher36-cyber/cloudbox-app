pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/yogeshmeher36-cyber/cloudbox-app.git'
            }
        }
        stage('Build Docker') {
            steps {
                echo 'Building Docker image...'
                sh 'docker-compose build'
            }
        }
        stage('Run Docker') {
            steps {
                echo 'Starting Docker containers...'
                sh 'docker-compose up -d'
            }
        }
    }
}
