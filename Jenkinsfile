pipeline{
    agent any

    tools{
        gradle 'Gradle8.7'
        nodejs 'Node21'
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