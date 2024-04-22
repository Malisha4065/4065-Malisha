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
                sh 'cd backend'
                sh 'docker build -t frontend .'
                sh 'cd ../frontend'
                sh 'docker build -t backend .'
            }
        }

        stage('Run') {
            steps {
                sh 'docker run -p 5173:5173 frontend'
                sh 'docker run -p 5555:5555 backend'
            }
        }
    }
}