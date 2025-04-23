pipeline {
    agent any

    tools {
        gradle 'gradle'  // This matches the name configured in Jenkins Global Tools
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'feature/login', url: 'https://github.com/TedlaHaneesh/devops-scenario1.git'
            }
        }

        stage('Build') {
            steps {
                sh './gradlew clean build'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // You can add additional testing steps here if needed
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // You can add your deployment steps here
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
        }
    }
}
