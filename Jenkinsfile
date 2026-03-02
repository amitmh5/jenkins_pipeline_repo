pipeline{
     agent any
     
    stages{
        stage('stage1'){
            steps{
                 sh 'sleep 5'
                 echo "This is the stage 1"
            }
        }
         stage('stage2'){
            steps {
                sh '''
                     #!/bin/bash
                     pwd
                     ls -lrt
                     sleep 5
                 ''' 
                 echo "this is  the stage 1" 
           }
        }
    }
}