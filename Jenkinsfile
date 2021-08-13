

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
                deploy adapters: [tomcat9(credentialsId: '661e4c32-971a-4dea-a8a0-29a48623eb7f', path: '', url: 'http://13.234.186.165:8080/')], contextPath: 'demo', war: '**/demoWebAPP-1-SNAPSHOT'
            }
        }
    }
}
