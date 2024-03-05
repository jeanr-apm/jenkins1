pipeline{
    agent any

    stages{
        stage('Build and Test'){
            matrix{
                axes{
                    axis{
                        name 'PLATFORM'
                        values 'Linux', 'MacOs', 'Windows'
                    }
                    axis{
                        name 'BROWSER'
                        values 'Safari', 'Firefox', 'Chrome'
                    }
                }
                stages{
                    stage('Build'){
                        steps{
                            echo "Build for ${PLATFORM} - ${BROWSER}"
                        }
                    }
                    stage('Test'){
                        steps{
                            echo "Test for ${PLATFORM} - ${BROWSER}"
                        }
                    }
                }
            }

        }

        stage('Deployment'){
            steps{
                echo 'Deploying app...'
            }
        }

    }
}