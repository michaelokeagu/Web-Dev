pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', 
                    credentialsId: '50d22cdd-36e1-4e5d-821e-c44674b31128', 
                    url: 'https://github.com/michaelokeagu/Web-Dev.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the project...'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application... Please wait'
            }
        }
    }
}
