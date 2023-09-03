pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build and Push Docker Image') {
            steps {
                script {
                    // Build and tag the Docker image
                    sh 'docker build -t my-rancher-app .'
                    
                    // Push the Docker image to a container registry
                    sh 'docker push my-registry/my-rancher-app:latest'
                }
            }
        }
        stage('Deploy to Rancher') {
            steps {
                // Add Rancher deployment commands here
            }
        }
    }
}