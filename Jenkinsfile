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
        
        // Add additional stages here, e.g., Build, Deploy
        stage('Build Docker Image') {
            steps {
                // Your build steps here
            }
        }
        
        stage('Push to Docker Hub') {
            steps {
                // Your push steps here
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                // Your deploy steps here
            }
        }
    }
}
