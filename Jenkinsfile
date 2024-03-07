pipeline {
    agent any
    stages {
        // stage('Clone repository') {
        //     steps {
        //         checkout([$class: 'GitSCM',
        //                   branches: [[name: '*/main']],
        //                   userRemoteConfigs: [[url: 'https://github.com/Jatinsharma159/Jenkins.git']])
        //     }
        // }
        stage('Build') {
            steps {
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
            error 'Pipeline failed'
        }
    }
}
