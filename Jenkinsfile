pipeline {
    agent any
    triggers {
        pollSCM('H/1 * * * *') // Poll GitHub every minute
    }
    stages {
        stage('Checkout') {
            steps {
                echo 'Stage 1: Checkout latest code from GitHub'
                git branch: 'main', url: 'https://github.com/Tamil5102000/8.1C-Task1.git'
            }
        }
        stage('Build') {
            steps { echo 'Stage 2: Build the project'; sh 'echo "Building project..."' }
        }
        stage('Code Quality Check') {
            steps { echo 'Stage 3: Run code quality analysis'; sh 'echo "Checking code quality..."' }
        }
        stage('Unit Testing') {
            steps { echo 'Stage 4: Run unit tests'; sh 'echo "Executing unit tests..."' }
        }
        stage('Integration Testing') {
            steps { echo 'Stage 5: Run integration tests'; sh 'echo "Executing integration tests..."' }
        }
        stage('Deployment to Staging') {
            steps { echo 'Stage 6: Deploy to staging environment'; sh 'echo "Deploying to staging..."' }
        }
        stage('Notification') {
            steps { echo 'Stage 7: Send notification to team'; sh 'echo "Sending notification..."' }
        }
    }
}
