pipeline{
    agent any

    stages{
        stage('Build'){
            steps{
                sh 'echo hello > world.txt'
                archiveArtifact(artifacts: '*.txt')
            }
        }
    }

}