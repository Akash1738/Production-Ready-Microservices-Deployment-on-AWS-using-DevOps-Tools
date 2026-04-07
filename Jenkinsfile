pipeline {
    agent any
    stages {
        stage('Clone Code') {
            steps {
                git 'https://github.com/Akash1738/Production-Ready-Microservices-Deployment-on-AWS-using-DevOps-Tools.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Docker Build') {
            steps {
                sh 'docker build -t myapp .'
            }
        }
        stage('Push to DockerHub') {
            steps {
                sh 'docker tag myapp akash1738/myapp:latest'
                sh 'docker push akash1738/myapp:latest'
            }
        }
    }
}
