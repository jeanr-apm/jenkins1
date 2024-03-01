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
            branch 'master'
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