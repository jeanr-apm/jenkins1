pipeline{
    agent any

    environment {
        DEPLOY_TO = 'production'
    }

    
    stages{
        stage('build'){
            steps {
                echo 'build!'
            }
        }

        stage('deployment'){
           when{
            allOf{
                branch 'master'
                environment name: 'DEPLOY_TO', value: 'production'
            }
           }
           
           steps{
            echo 'Deploy !'
           }
        }
        
    }

    post{
        always{
            echo 'Always!!!'
        }
        success{
            echo 'Success!!!'
        }
    }
}