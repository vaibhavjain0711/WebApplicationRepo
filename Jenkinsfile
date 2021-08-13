

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
                deploy adapters: [tomcat9(credentialsId: '661e4c32-971a-4dea-a8a0-29a48623eb7f', path: '', url: 'http://localhost:8081/')],
                    contextPath: 'api/hello', onFailure: false, war: '**/demoHelloSpring-0.0.1-SNAPSHOT.war'
            }
        }
        
       
       
    }
}
