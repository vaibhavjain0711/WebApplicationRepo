

pipeline {
    agent any
    
    stages {
        
         stage('java version') {
            steps {
                bat 'java -version'
            }
        }
        
         stage('maven version') {
            steps {
                bat 'mvn -version'
            }
        }
       
        stage('build clean') {
            steps {
                bat 'mvn clean'
            }
        }
        
         stage('build package') {
            steps {
                bat 'mvn package'
            }
        }
   
         stage('deploying') {
            steps {
               deploy adapters: [tomcat9(credentialsId: '102', path: '', url: 'http://localhost:8081/')], contextPath: '/api/hello', war: '**/demoHelloSpring-0.0.1-SNAPSHOT.war'
            }
        }
        
       
       
    }
}
