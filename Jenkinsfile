pipeline {
    agent any
    environment {
        NODE_ENV = 'development'
    }
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/david0125q/sample-node-app.git', branch: 'main'
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
        stage('Build') {
            steps {
                sh 'npm run build' // Adjust this step if you have a build process
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying application..."'
                // Add your deployment commands here
            }
        }
    }
    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
