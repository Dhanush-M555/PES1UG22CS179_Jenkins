pipeline {
    agent any
    stages {
        // stage('Clone repository') {
        //     steps {
        //         git branch: 'main', url: 'https://github.com/<your-username>/<your-repo>.git'
        //     }
        // }
        stage('Build') {
            steps {
                sh 'g++ main/hello.cpp -o main/hello_exec'
                echo 'Build stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh './mainly/hello_exec'
                echo 'Test Stage Successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}