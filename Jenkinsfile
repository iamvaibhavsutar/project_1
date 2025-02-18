pipeline {
    agent any
    stages {
        stage('Checkout SCM') {
            steps {
                script {
                    checkout scm: [
                        $class: 'GitSCM',
                        branches: [[name: '*/main']],  // Ensure 'main' is the correct branch
                        userRemoteConfigs: [[url: 'https://github.com/iamvaibhavsutar/project_1.git']]
                    ]
                }
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    echo 'Building Docker image...'
                    // Add actual Docker build command here
                }
            }
        }

        stage('Push to Docker Hub') {
            steps {
                script {
                    echo 'Pushing Docker image to Docker Hub...'
                    // Add actual Docker push command here
                }
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                script {
                    echo 'Deploying to Kubernetes...'
                    // Add actual Kubernetes deploy command here
                }
            }
        }
    }
}
