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
                // Your build steps here, for example:
                script {
                    echo 'Building Docker image...'
                    // Add actual Docker build command here
                }
            }
        }

        stage('Push to Docker Hub') {
            steps {
                // Your push steps here, for example:
                script {
                    echo 'Pushing Docker image to Docker Hub...'
                    // Add actual Docker push command here
                }
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                // Your deploy steps here, for example:
                script {
                    echo 'Deploying to Kubernetes...'
                    // Add actual Kubernetes deploy command he

