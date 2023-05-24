pipeline {
  agent any
  
  stages {
    stage('build code') {
      steps {
        // Run tests for the application
        bat 'mvn clean install'
      }
    }
    
    stage('Test code') {
      steps {
        bat 'mvn test'
      }
    }
    
    stage('Deploy code') {
      steps {
       bat 'xcopy target\\*.war "C:\\Program Files\\Apache Software Foundation\\Tomcat 10.1\\webapps" /Y'

      }
    }
    
  }
}