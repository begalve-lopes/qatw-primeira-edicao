pipeline {
    agent {
        dockerContainer {
            image 'mcr.microsoft.com/playwright:v1.60.0-noble'
        }
    }

    stages {

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('E2E Tests') {
            steps {
                sh 'npx playwright test'
            }
        }
    }
}