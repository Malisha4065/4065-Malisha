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
                sh 'cd backend && docker build -t frontend .'
                sh 'cd frontend && docker build -t backend .'
            }
        }

        stage('Run') {
            steps {
                sh 'docker run -p 5173:5173 frontend && docker run -p 5555:5555 backend'
            }
        }
    }
}