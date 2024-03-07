pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                checkout scm
                build 'PES2UG21CS143-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
                // Add deployment steps here if needed
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
