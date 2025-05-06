pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/Navi126/pipline.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t flask-cicd-app .'
            }
        }

        stage('Run with Docker Compose') {
            steps {
                sh 'docker-compose down'
                sh 'docker-compose up -d --build'
            }
        }
    }
}

