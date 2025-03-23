pipeline {
    agent any
    when {
        changeRequest()
    }
    stages {
        stage('Test') {
            steps {
                echo "Running PR build for branch: ${env.BRANCH_NAME}"
            }
        }
    }
}
