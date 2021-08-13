

pipeline {
    agent any
    
    stages {
        
         stage('java version') {
            steps {
                sh 'java -version'
            }
        }
        
         stage('maven version') {
            steps {
                sh 'mvn --version'
            }
        }
       
        stage('build clean') {
            steps {
                sh 'mvn clean
            }
        }
        
        stage('build package') {
            steps {
                sh 'mvn package'
            }
        }
        
       
       
    }
}
