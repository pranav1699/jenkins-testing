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
        script{
        def PROJ = "${PROJECT}"
        def data = readFile(file: 'test.yml')
        bat "echo ${PROJ}"
        println(data)
        }
        bat "echo ${PROJECT}"
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
