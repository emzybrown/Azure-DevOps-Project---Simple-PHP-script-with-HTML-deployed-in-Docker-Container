pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git credentialsId: 'github-token', url: 'https://github.com/emzybrown/Azure-DevOps-Project---Simple-PHP-script-with-HTML-deployed-in-Docker-Container', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                // Add your build steps here
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                // Add your test steps here
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                // Add your deploy steps here
                echo 'Deploying...'
            }
        }
    }
}
