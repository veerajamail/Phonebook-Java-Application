@Library('jenkins-library@main') _

pipeline {
    agent any
    stages {
        stage('Git Checkout') {
            steps {
            gitCheckout(
                branch: "main",
                url: "https://github.com/veerajamail/Phonebook-Java-Application.git"
            )
            }
    }
        stage('Notify') {
            steps {
                script {
                    notify(recipients: 'janavlearn@example.com')
                }
            }
        }
    }

    post {
        success {
            script {
                notify(recipients: 'janavlearn@example.com')
            }
        }
        failure {
            script {
                notify(recipients: 'janavlearn@example.com')
            }
        }
    }
}

