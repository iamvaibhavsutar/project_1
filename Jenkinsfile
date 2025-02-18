pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
			git credentialsId: 'jen_1', url: 'https://github.com/iamvaibhavsutar/project_1.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t your-dockerhub-username/video-streaming:latest .'
            }
        }
        stage('Push to Docker Hub') {
            steps {
                sh 'docker login -u your-dockerhub-username -p your-password'
                sh 'docker push your-dockerhub-username/video-streaming:latest'
            }
        }
        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f deployment.yaml'
            }
        }
    }
}

