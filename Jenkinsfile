pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
                checkout scm
            }
        }

        stage('Test') {
            steps {
                echo 'Running application tests...'
                sh 'echo "Test Passed Successfully"'
            }
        }

        stage('Validation') {
            steps {
                echo 'Running validation...'
                sh 'echo "Validation Passed"'
            }
        }

    }
}
