// Jenkinsfile
pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/your-username/web-simple.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-web-cicd .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker rm -f my-web || true'
                sh 'docker run -d --name my-web -p 8080:80 my-web-cicd'
            }
        }
    }
}
