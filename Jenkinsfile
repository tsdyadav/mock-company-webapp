pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building...'
                }
                sh './gradlew assemble'
            }
        }
        stage('Test') {
            steps {
                script {
                    echo 'Running Tests...'
                }
                sh './gradlew test'
            }
        }
    }
    post {
        success {
            echo 'Build and test succeeded!'
        }
        failure {
            echo 'Build or test failed!'
        }
    }
}
