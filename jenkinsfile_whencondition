pipeline{
    agent any
     
    parameters{
        booleanParam(name: 'DEPLOY', description: 'want to deploy to Production')
    }
    
    environment{
        CURRRENT_ENV = 'prodaa'
    }

     

    stages{
        stage('stage1 when branch main'){
            when{
                branch 'main'
            }
            steps{
                
                echo "This is stage1 running"
                sh '''
                  sleep 5
                  exit 1
                  '''
                
            }
        }
         stage('when environment'){
            when{
                environment name:'CURRENT_ENV', value:'prod'
            }
                    steps{
                       echo 'This is final running'
                       sh 'sleep 5'
                    }
                }
        stage('when parameter'){
            when{
                expression {params.DEPLOY == true}
            }
            steps{
                echo " This is final running"
                sh'sleep 5'
            }
           
        }
       

         
    }
}