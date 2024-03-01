pipeline{
    agent any

    parameters {
        booleanParam(name: 'DEPLOY_TO', defaultValue: false, description: 'Are you sure you want to deploy?')
    }

    
    stages{
        stage('build'){
            failFast true
            parallel {
                stage('build frontend'){
                    steps {
                        echo 'build frontend'
                    }
                }

                stage('build backend'){
                    steps {
                        echo 'build backend'
                    }
                }
            }
        }

        stage('deployment'){
           when{
            anyOf{
                branch 'masterx'
                expression {params.DEPLOY_TO}
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