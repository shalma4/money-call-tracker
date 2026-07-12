pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Code downloaded from GitHub'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t money-tracking:v1 .'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker run --rm money-tracking:v1'
            }
        }
        stage('Debug') {
    steps {
        bat 'type C:\\Users\\prima\\.kube\\config'
    }
}
        stage('Deploy to Kubernetes') {
    steps {
        bat 'kubectl apply -f deployment.yaml'
    }
}
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}
