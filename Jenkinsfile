pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps { git 'https://github.com/michellemontoya/ejemplo-java.git' }
        }
        stage('Build') {
            steps { sh './mvnw clean package' }
        }
        stage('Test') {
            steps { sh './mvnw test' }
        }
    }
}
