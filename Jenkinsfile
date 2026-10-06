pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo "Building branch: ${env.BRANCH_NAME}"
            }
        }
        stage('Build') {
            steps {
                echo 'Building application...'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }
        stage('Deploy') {
            when {
                branch 'main' // Only runs when building the main branch
            }
            steps {
                echo 'Deploying to production environment...'
            }
        }
    }
}
