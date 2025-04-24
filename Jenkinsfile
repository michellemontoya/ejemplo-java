pipeline {
    agent any

    tools {
        maven 'maven-3.9.9'
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/michellemontoya/ejemplo-java.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                script {
                    try {
                        sh 'mvn clean package'
                    } catch (Exception e) {
                        currentBuild.result = 'FAILURE'
                        throw e
                    }
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    try {
                        sh 'mvn test'
                    } catch (Exception e) {
                        currentBuild.result = 'FAILURE'
                        throw e
                    }
                }
            }
        }
    }
}
