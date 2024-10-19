pipeline {
    agent {
        docker { image 'node:14' }  // Use Node.js Docker image for the build
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'  // Run npm install to install dependencies
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'  // Run tests using npm
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-app .'  // Build Docker image of the application
            }
        }
    }
}

