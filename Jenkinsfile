pipeline{
    agent any

    
    stages{
        stage('build'){
            steps {
                echo 'build!'
            }
        }

        stage('deployment'){
           when{
            branch 'prod'
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