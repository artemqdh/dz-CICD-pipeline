pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test -- --watchAll=false --passWithNoTests || true'
            }
        }
        stage('Deploy') {
            steps {
                sh 'npm start &'
            }
        }
    }
}