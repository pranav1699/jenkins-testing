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
        type test.yaml 
        '''
    }
    stage('Deploy') { 
        bat '''
        echo 'hello world '
        '''
    }
}
