pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/KevinAbraham07/Jenkins.git'
            }
        }

        stage('Compile') {
            steps {
                bat 'javac Hello.java'
            }
        }

        stage('Run') {
            steps {
                bat 'java Hello'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: '*.class'
            }
        }
    }

    post {
        failure {
            echo 'Build failed!'
        }
    }
}
