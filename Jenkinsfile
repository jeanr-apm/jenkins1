pipeline{
    agent any

    

    stages{
        stage('Build'){
            steps{
                echo 'hello'
            }
        }
    }
    post{
        success {
            emailext(to: 'jrhodelyr@gmail.com', body: 'Test: Sending email from Jenkins', subject: 'Jenkins - Email Notification')
        }
    }

}