pipeline{
    agent any

     

    stages{
        stage('stage1'){
            steps{
                catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE'){
                echo "This is stage1 running"
                sh '''
                  sleep 5
                  exit 1
                  '''
                }
            }
        }
        stage('PARALLEL TESTING'){
            parallel{
                stage('WINDOWS TESTING'){
                    steps{
                        echo "This is windows running"
                        sh 'sleep 5'
                        
                    }
                }

                stage('MAC TESTING'){
                    steps{
                        echo "This is macos running"
                        sh 'sleep 10'
                    }
                }
            }
           
        }
        stage('final'){
                    steps{
                        echo "This is final running"
                        sh 'sleep 5'
                    }
                }

         
    }
}