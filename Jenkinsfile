pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code
                git 'https://github.com/kingtheraja/kingthearaja.git'
            }
        }
        
        stage('Build') {
            steps {
                // Build the project using Maven
                bat 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Run tests using Maven
                bat 'mvn test'
            }
        }

        stage('Package') {
            steps {
                // Package the project (if needed)
                bat 'mvn package'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the project (customize this for your needs)
                echo 'Deploying...'
                // e.g., bat 'scp target/my-app.jar user@server:/path/to/deploy'
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
