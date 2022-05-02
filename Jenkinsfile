stage('Build') {
    bat ' docker version '
    bat 'docker info'
    bat 'docker compose version'
}

stage('Test') {
    windows: {
        node('windows') {
            bat '''
          type test.yml 
        '''
        }
    }
}
