pipeline {
    agent any
    
    stages {
        stage('Checking Version') {
            steps {
                bat 'javac -version'
            }
        }
        stage('Compiling') {
            steps {
                bat 'javac Hello.java'
            }
        }
        
        stage('Running') {
            steps {
                bat 'java Hello'
            }
        }
    }
}
