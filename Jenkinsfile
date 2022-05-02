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
        type > test.txt
        '''
    }
    stage('Deploy') { 
        bat '''
        bat echo 'hello wrold '
        '''
    }
}
