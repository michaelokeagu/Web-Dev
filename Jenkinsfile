pipeline {
    agent any                 // Step 1: Use any available Jenkins agent
    stages {
        stage('Checkout') {   // Step 2: Clone the repository
            steps {
                echo 'Cloning the repository...'
                checkout scm
            }
        }
        stage('Build') {      // Step 3: Build the project
            steps {
                echo 'Building the project...'
                sh 'ls -al' // Check files
                sh 'chmod +x gradlew'
                sh './gradlew build'
            }
        }
        stage('Test') {       // Step 4: Run tests
            steps {
                echo 'Running tests...'
                sh './gradlew test'
            }
        }
        stage('Deploy') {     // Step 5: Deploy the application
            steps {
                echo 'Deploying the application...'
                sh './deploy.sh'
            }
        }
    }
    post {                   // Step 6: Handle the pipeline result
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
