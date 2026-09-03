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
                echo 'Verifying Python is available...'
                sh 'python3 --version'
            }
        }
        stage('Test') {
            steps {
                echo 'Running the app...'
                sh 'python3 app.py'
            }
        }
        stage('Validation') {
            steps {
                echo 'Validating output...'
                sh '''
                    OUTPUT=$(python3 app.py)
                    echo "Got: $OUTPUT"
                    if [ "$OUTPUT" != "Hello World" ]; then
                        echo "Validation failed: unexpected output"
                        exit 1
                    fi
                    echo "Validation passed"
                '''
            }
        }
    }
}
