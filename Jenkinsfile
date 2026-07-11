pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code...'
            }
        }

        stage('Run Python Program') {
            steps {
                bat '"C:\\Users\\prima\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" calculate.py'
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
