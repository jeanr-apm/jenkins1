pipeline{
    agent any

    tools{
        gradle 'Gradle8.7'
        node 'Nodejs21.6'
    }

    stages{
        stage('Build'){
            steps{
                sh 'gradle -v'
                sh 'node -v'
            }
        }
    }

}