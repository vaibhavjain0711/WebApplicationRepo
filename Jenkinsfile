

pipeline {
    agent any
    
    stages {
        stage('Checking Version') {
            steps {
                bat 'javac -version'
            }
        }
        stage('build') {
            steps {
                bat 'mvn clean package'
            }
        }
        
        stage('deploying') {
            steps {
                bat 'deploying process PENDING'
            }
        }
    }
}
