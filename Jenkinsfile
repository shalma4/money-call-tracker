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
                bat 'docker build -t money-tracker:v1 .'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker run --rm money-tracker:v1'
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
