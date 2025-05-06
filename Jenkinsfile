pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                https://github.com/Navi126/Docker_file.git
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

#Testing
