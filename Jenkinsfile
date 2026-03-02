pipeline{
    agent none

     parameters{
        string(name: 'NAME',defaultValue: '',description:'')
        booleanParam (name: 'SKIP_TEST',description:'')
        choice(name: 'BRANCH',choices: ['master','staging','prod'],description:'')
     }

    stages{
        stage('stage1'){

            agent { label 'slave1ubuntu'}
            steps{
                echo "NAME: ${params.NAME}"
                echo "SKIP_TEST: ${params.SKIP_TEST}"
                echo "BRANCH TO DEPLOY: ${params.BRANCH}"
                   
            }
        }
         
    }
}