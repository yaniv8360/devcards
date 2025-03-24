pipeline {
    agent any

    triggers {
        // This is used for GitHub webhook trigger
        githubPush()
    }

    options {
        disableConcurrentBuilds() // Avoid multiple concurrent builds
    }

    stages {
        stage('Checkout') {
            when {
                branch 'develop'
            }
            steps {
                echo "Checking out code from develop branch"
                checkout scm
            }

            
        }

        stage('Build') {
            when {
                branch 'develop'
            }
            steps {
                echo "Building the app..."
                // Example: sh 'npm install'
            }
        }

        stage('Test') {
            when {
                branch 'develop'
            }
            steps {
                echo "Running tests..."
                // Example: sh 'npm test'
            }
        }

        stage('Deploy de') {
            when {
                branch 'develop'
            }
            steps {
                echo "Deploying the app..."
                // Example: sh './deploy.sh'
            }


            
        }
    }
}
