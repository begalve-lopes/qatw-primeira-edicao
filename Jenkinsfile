pipeline {
    agent {
        docker {
            image 'mcr.microsoft.com/playwright:v1.60.0-noble'
        }
    }

    options {
        timeout(time: 20, unit: 'MINUTES')
    }

    stages {

        stage('Install Dependencies') {
            steps {
                sh 'npm ci'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npx playwright test --reporter=line'
            }
        }
    }
}