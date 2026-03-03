pipeline{
    agent any

     environment{
        DOCKER_USER = 'amitmh'
        AWS_ACCESS_KEY = '1234'
     }

    stages{
        stage('stage1'){
            steps{
                echo "DOCKER_USER: ${env.DOCKER_USER}"
                echo "SKIP_AWS_ACCESS_KEYTEST: ${env.AWS_ACCESS_KEY}"
                
                
                sh '''
                    env
                    echo $DOCKER_USER
                '''
            }
        }
         
    }
}