pipeline {
    agent any

    tools {
        nodejs "NodeJS-18" // Ensure this tool is configured in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/thatchayaini-p/reactoldjs.git', credentialsId: 'thatchayaini-p/******(new personal token)'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }

        stage('Build React App') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add deployment logic here (e.g., copying to server or S3)
            }
        }
    }
}
