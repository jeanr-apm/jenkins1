pipeline{
    agent {
        docker {
            image 'node:21-alpine'
        }
    }

    

    stages{
        stage('build'){
            steps {
                
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