pipeline{
    agent any

    
    stages{
        stage('build'){
            steps {
                echo 'build!'
            }
        }

        stage('deployment'){
            input {
                message 'Are you sure you want to deploy?'
                ok 'Deploy'
                submitter 'admin, devops'
                submitterParameter 'USER_SUBMIT'
                parameters {
                    string(name: 'VERSION', defaultValue: 'latest', description: 'App version')
                }
            }
            steps {
                echo "User: ${USER_SUBMIT}"
                echo "Version: ${VERSION}"
                echo 'Deploy!'
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