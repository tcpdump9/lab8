pipeline{
    agent any
    environment {
        REGISTRY = "docker.io/tcpdump9/lab8"
        IMAGE_TAG = "${env.BUILD_NUMBER}"
    }
    stages{
        stage('Checkout'){
            steps{
                checkout scm
            }
        }
        stage('Tests'){
            steps{
                sh 'npm install --silent || true'
                sh 'npm test'
            }
        }
        stage('Build docker'){
            steps{
                script{
                    dockerImage = docker.build("${REGISTRY}:${IMAGE_TAG}")
                }
            }
        }
    }
}