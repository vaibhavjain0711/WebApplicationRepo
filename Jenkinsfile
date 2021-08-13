

pipeline {
    agent any
    
    stages {
        stage('Checking Version') {
            steps {
                sh 'mvn --version'
            }
        }
        stage('build') {
            steps {
                sh 'mvn clean package'
            }
        }
        
        stage('deploying') {
            steps {
                sh 'deploying process PENDING'
            }
        }
    }
}
