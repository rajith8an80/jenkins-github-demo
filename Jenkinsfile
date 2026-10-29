pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'python3 --version'
            }
        }

        stage('Test') {
            steps {
                echo 'Running the Python application...'
                sh 'python3 hello.py'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment completed successfully!'
            }
        }
    }

    post {
        success {
            echo 'Jenkins Pipeline SUCCESS!'
        }
        failure {
            echo 'Jenkins Pipeline FAILED!'
        }
    }
}
