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

    environment {
        TZ = 'America/New_York'
    }

    stages{
        stage('build'){

            options {
                timestamps()
            }
            steps {
                echo 'This is a test 2'
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