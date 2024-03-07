pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                // Intentional error to simulate a failing test
                sh './output_fake'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
            error 'Pipeline failed'
        }
    }
}
