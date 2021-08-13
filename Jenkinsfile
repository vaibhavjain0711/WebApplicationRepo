

pipeline {
    agent any
    
    stages {
        stage('Checking Version') {
            steps {
                bat 'java -version'
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
