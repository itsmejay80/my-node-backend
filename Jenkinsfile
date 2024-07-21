pipeline {
    agent any

   tools{
        nodejs '22.5.1'
   }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                git branch: 'main', url: 'https://github.com/itsmejay80/my-node-backend.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                // Install Node.js dependencies
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                // Run tests
                sh 'npm test'
            }
        }

        stage('Build') {
            steps {
                // Placeholder for build steps, if any
                echo 'Building...'
            }
        }

        stage('Deploy') {
            steps {
                // Placeholder for deploy steps, customize as needed
                echo 'Deploying...'
                // Example: scp or rsync to deploy files to a server
                // sh 'scp -r * user@your-server:/path/to/deployment'
            }
        }
    }

    post {
        always {
            // Clean up workspace
            cleanWs()
        }
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
