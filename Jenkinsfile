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
    stage('Start containers') {
      steps {
        bat 'docker-compose up -p amalga -d'
        bat 'docker-compose ps'
      }
    }
    
  }
}
