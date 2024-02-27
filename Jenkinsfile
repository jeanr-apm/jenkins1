pipeline{
    agent any

    options{
        timeout(time:1, unit:'HOURS')
    }

    environment {
        TZ = 'America/New_York'
    }

    parameters {
        string(name: 'NAME', defaultValue: 'Rhodelyr Jean', description: 'Please enter your name')
        text(name: 'EMPLOYER', defaultValue: 'MPA', description: 'Please enter your employer')
        booleanParam(name: 'JOB', defaultValue: true, description: 'Full-time job')
        choice(name: 'SALARY', choices: ['<50,000', '50,001 - 100,000','100,001 - 150,000'])
        password(name:'PIN', description: 'Please enter your pin number')

    }

    stages{
        stage('build'){

            options {
                timestamps()
            }
            steps {
                echo "NAME: ${NAME}"
                echo "EMPLOYER: ${EMPLOYER}"
                echo "JOB: ${JOB}"
                echo "SALARY: ${SALARY}"
                echo "PIN: ${PIN}"
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