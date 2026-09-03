pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from GitHub...'
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'npm install'   
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'npm test'   
            }
        }
        stage('Validation') {
            steps {
                echo 'Running validation checks...'
                sh 'npm run lint'   
            }
        }
    }
}}
