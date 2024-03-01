pipeline{
    agent any

    options {
        parallelAlwaysFailFast()
    }

        
    stages{
        stage('build'){
            //failFast true
            parallel {
                stage('build frontend'){
                    steps {
                        echo 'build frontend'
                    }
                }

                stage('build backend'){
                    steps {
                        echo "${VARIABLE}"
                        echo 'build backend'
                    }
                }
            }
        }

        stage('deployment'){
           when{
            anyOf{
                branch 'master'
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