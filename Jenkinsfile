pipeline{
    agent any
     
    parameters{
        booleanParam(name: 'DEPLOY', description: 'want to deploy to Production')
    }
    
    environment{
        CURRENT_ENV = 'prod'
    }

     

    stages{
        stage('CHECKOUT_REPOA'){
            steps{
                checkout ([ $class: 'GitSCM',
                branches: [[name: '*/main']], 
                extensions: [],
                userRemoteConfigs: [[
                    credentialsId: 'hp-git',
                    url: 'https://github.com/amitmh5/jenkins_pipeline_repo.git'
                ]]
                ])

                sh '''
                    echo GIT_BRANCH: $GIT_BRANCH
                    echo BRANCH_NAME: $BRANCH_NAME
                '''

            }
        }
        stage('stage1 when branch main'){
            when{
                expression{
                    return env.GIT_BRANCH == 'origin/main'
                }
               
            }
            steps{
                
                echo "This is stage1 running"
                sh '''
                  pwd
                  ls -lrt
                  sleep 5
                  
                  '''
                
            }
        }
         stage('when environment'){
            when{
                environment name:'CURRENT_ENV', value:'prod'
            }
                    steps{
                       echo 'This is final running'
                       sh '''
                  pwd
                  ls -lrt
                  sleep 5
                  
                  '''
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