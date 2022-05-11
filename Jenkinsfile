pipeline {
  agent any
 
  
  stages {
    stage("verify tooling") {
      steps {
        bat '''
          docker version
          docker info
          docker compose version 
        '''
      }
    }
    stage("printing yaml file") {
      steps {
        environment {
          PROJ = "${PROJECT}"
        }
        bat "echo ${PROJECT}"
        bat "echo ${PROJ}"
        bat "type .env"
        bat '''
          type test.yml 
        '''
        
      }
    }
    stage("printing txt file from diff dir") {
      steps {
        dir('etc') {
        bat "type test.txt"
        } 
      }
    }
    stage("echo env variables") {
      steps {
        bat "echo ${PROJECT}"
      }
    }
    stage('Start containers') {
      steps {
        bat 'docker-compose -p amalga up -d'
        bat 'docker-compose ps'
      }
    }
    
  }
}
