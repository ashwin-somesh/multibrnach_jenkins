pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo "Checking out the source code..."
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Building the project..."
                sh 'echo "Build successful!"'
                // Example: sh 'mvn clean package' or 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                sh 'echo "All tests passed!"'
                // Example: sh 'mvn test' or 'pytest tests/'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying the application..."
                sh 'echo "Application deployed successfully!"'
                // Example: sh 'scp target/app.war user@server:/var/www/html/'
            }
        }
    }

    post {
        always {
            echo "Cleaning up workspace..."
            cleanWs()
        }
        success {
            echo "✅ Pipeline executed successfully!"
        }
        failure {
            echo "❌ Pipeline failed!"
        }
    }
}
