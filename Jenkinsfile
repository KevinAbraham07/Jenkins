pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Running build stage'
            }
        }
    }

    post {
        success {
            echo 'Build completed successfully!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
