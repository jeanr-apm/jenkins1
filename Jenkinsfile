pipeline{
    agent any

    

    stages{
        stage('Build'){
            steps{
                
            }
        }
    }
    post{
        success {
            emailext(to: 'jrhodelyr@gmail.com', body: 'Test: Sending email from Jenkins', subject: 'Jenkins - Email Notification')
        }
    }

}