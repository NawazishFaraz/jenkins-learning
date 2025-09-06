pipeline {
    agent any  // run on any available agent/node

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/NawazishFaraz/jenkins-learning.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building project..."'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploy step (dummy)"'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully ✅'
        }
        failure {
            echo 'Pipeline failed ❌'
        }
    }
}

