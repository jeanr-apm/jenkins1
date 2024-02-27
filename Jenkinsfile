pipeline{
    /*agent {
        docker {
            image 'node:21-alpine'
        }
    }*/
    agent any

    options{
        timeout(time:1, unit:'HOURS')
    }

    stages{
        stage('build'){

            options {
                timestamps()
            }
            steps {
                echo 'This is a test'
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