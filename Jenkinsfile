@Library('sharedlibrary') _

pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    checkout([
                        $class: 'GenericSCMStep',
                        scm: [
                            $class: 'GitSCM',
                            branches: [[name: '*/main']],
                            doGenerateSubmoduleConfigurations: false,
                            extensions: [],
                            userRemoteConfigs: [[url: 'https://github.com/your-repo.git', credentialsId: 'your-credentials-id']]
                        ]
                    ])
                }
            }
        }

        // stage('Build') {
        //     steps {
        //         //sh './gradlew clean build' // or 'mvn clean install' for Maven projects
        //     }
        // }

        // stage('Test') {
        //     steps {
        //         //sh './gradlew test' // or 'mvn test' for Maven projects
        //     }
        // }

        // stage('Deploy') {
        //     steps {
        //         echo 'Deploying to the server...'
        //         // Add deployment steps here
        //     }
        // }
    }
}
