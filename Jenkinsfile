pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'cd backend && docker build -t backend .'
                sh 'cd frontend && docker build -t frontend .'
            }
        }

        stage('Run') {
            steps {
                sh 'docker run -d -p 5555:5555 backend'
                sh 'docker run -d -p 5173:5173 frontend'
            }
        }
    }
}