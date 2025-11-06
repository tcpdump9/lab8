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
    }
}