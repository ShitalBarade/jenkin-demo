pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Starting source code checkout'
                checkout scm
                echo 'Source code checkout completed'
            }
        }

        stage('Build') {
            steps {
                echo 'Starting build stage'
                sh 'pwd'
                sh 'ls -la'
                echo 'Build stage completed'
            }
        }

        stage('Test') {
            steps {
                echo 'Starting test stage'

                sh 'test -f README.md'

                echo 'README file exists'
                echo 'All tests passed'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully'
            }

        failure {
            echo 'Pipeline failed. Check Console Output.'
        }
    }
}
