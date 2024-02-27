pipeline{
    agent any

    options{
        timeout(time:1, unit:'HOURS')
    }

    triggers{
        cron('* * * * *')
    }

    stages{
        stage('build'){

            options {
                timestamps()
            }
            steps {
                echo 'Testing Cron trigger'
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