@Library("sharedlibrary@main") _

pipeline {
    agent any
    stages {
        stage('Code Checkout') {
            steps {
                script {
                  def workingDir = checkoutCode("https://github.com/veerajamail/Phonebook-Java-Application.git", "main")
                  echo $workingDir
                }
            }
        }
    }
}
