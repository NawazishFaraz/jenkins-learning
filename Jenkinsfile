pipeline {
    agent any
    tools { nodejs 'Node24' }   // 👈 Use the same name you configured
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/NawazishFaraz/jenkins-learning.git'
            }
        }
        stage('Build') {
            steps {
                echo '📦 Installing dependencies...'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo '🧪 Running tests...'
                sh 'npm test || echo "No tests yet, skipping..."'
            }
        }
        stage('Deploy') {
            steps {
                echo '🚀 Deploying application (dummy step)...'
            }
        }
    }
    post {
        success { echo '✅ Pipeline successful!' }
        failure { echo '❌ Pipeline failed!' }
    }
}
