node {  
    stage('Build') { 
        bat '''
        docker version
        docker info
        docker compose version
        '''
    }
    stage('Test') { 
        bat '''
        type test.yml 
        '''
    }
    stage('Deploy') { 
        bat '''
        echo 'hello world '
        '''
    }
}
