pipeline{
     agent { label 'slave1ubuntu'}

    stages{
        stage('stage1'){
            steps{
                echo "This is the stage 1"
                sh '''
                     sleep 5
                     echo "this is a linux command"
                   '''
                   
                 
            }
        }
         stage('build'){
            steps {
                echo "building java code"
                sh '''
                     #!/bin/bash
                     sleep 5
                 ''' 
                 
           }
        }
    }
}