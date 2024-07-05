@Library('sharedlibrary') _

pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    checkout(repoUrl: 'https://github.com/username/repository.git', branch: 'main', credentialsId: 'github-credentials')
                }
            }
        }

        stage('Build') {
            steps {
                //sh './gradlew clean build' // or 'mvn clean install' for Maven projects
            }
        }

        stage('Test') {
            steps {
                //sh './gradlew test' // or 'mvn test' for Maven projects
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to the server...'
                // Add deployment steps here
            }
        }
    }
}
