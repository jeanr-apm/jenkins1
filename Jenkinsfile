pipeline{
    agent any

    environment {
        MY_VAR = 'A variable'
        MY_NUMBER = 123456
    }

    stages{
        stage('build'){
            steps {
                echo 'Building application...'

                echo "BRANCH_NAME : ${env.BRANCH_NAME}"
                echo "BRANCH_IS_PRIMARY : ${env.BRANCH_IS_PRIMARY}"
                echo "CI : ${env.CI}"
                echo "BUILD_NUMBER : ${env.BUILD_NUMBER}"
                echo "JENKINS_URL : ${env.JENKINS_URL}"
                echo "MY_VAR : ${env.MY_VAR}"
                echo "MY_NUMBER : ${env.MY_NUMBER}"
                sh 'printenv'
            }
        }
        stage('tests'){
            steps{
                echo 'Running tests...'
            }
        }
        stage('deployment'){
            steps{
                echo 'Deploying application...'
            }
        }
        
    }
}