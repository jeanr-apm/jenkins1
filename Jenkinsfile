pipeline{
    agent any

    parameters {
        booleanParam(name: 'DEPLOY_TO', defaultValue: false, description: 'Are you sure you want to deploy?')
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
                equals expected: true, actual: params.DEPLOY_TO
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