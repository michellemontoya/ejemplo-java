pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/michellemontoya/ejemplo-java.git', branch: 'main'
            }
        }
        stage('Build') {
            steps { 
                sh 'mvn clean package' 
            }
        }
        stage('Test') {
            steps { 
                sh 'mvn test' 
            }
        }
    }
}
