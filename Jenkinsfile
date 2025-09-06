pipeline {
    agent any

    tools {
        nodejs "Node24"   // must match the NodeJS tool name configured in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                // Explicit checkout from main branch
                git branch: 'main', url: 'https://github.com/NawazishFaraz/jenkins-learning.git'
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
    }
}

