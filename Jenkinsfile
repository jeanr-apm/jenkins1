pipeline{
    agent any

    options{
        timeout(time:1, unit:'HOURS')
    }

    triggers{
        pollSCM('* * * * *')
    }

    stages{
        stage('build'){

            options {
                timestamps()
            }
            steps {
                echo 'Testing pollSCM trigger'
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