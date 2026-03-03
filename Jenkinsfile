pipeline{
    agent any

     environment{
        DOCKER_USER = 'amitmh'
        AWS_ACCESS_KEY = '1234'
     }

    stages{
        stage('stage1'){
            steps{
                echo "DOCKER_USER: ${DOCKER_USER}"
                echo "SKIP_AWS_ACCESS_KEYTEST: ${AWS_ACCESS_KEY}"
                
                
                sh '''
                    env
                    
                '''
            }
        }
         
    }
}