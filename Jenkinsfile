pipeline {
    agent any

    triggers {
        pollSCM('* * * * *')  // Polling every minute. Adjust as needed.
    }

    stages {
        stage('Checkout') {
            steps {
                script {
                    if (env.BRANCH_NAME == 'develop' || env.CHANGE_TARGET == 'develop') {
                        checkout scm
                    } else {
                        echo 'Not targeting develop, proceeding anyway...'
                        checkout scm
                    }
                }
            }
        }
        

        stage('Build') {
            steps {
                sh 'echo Building the project...'
            }
        }

        stage('Test') {
            steps {
                sh 'echo Running tests...'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo Deploying the project...'
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
            cleanWs()
        }
        success {
            echo 'Build completed successfully!'
        }
        failure {
            echo 'Build failed. Please check the logs.'
        }
    }
}
