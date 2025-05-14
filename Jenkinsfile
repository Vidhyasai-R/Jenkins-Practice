pipeline{
    agent{
        label 'AGENT-1'
    }

    environment{
        PROJECT = "EXPENSE"
        COMPONENT = "BACKEND"
    }

    options{
        disableConcurrentBuilds()
        timeout(time: 30, unit: 'MINUTES')
    }

    parameters{
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    stages{
        stage('Build'){
            steps{
                script{
                    sh """
                        echo "This is Build stage"
                        echo "Project: $PROJECT"
                        echo "Hello ${params.PERSON}"
                        echo "Hello ${params.BIOGRAPHY}"
                        sleep 15
                    """
                }
            }
        }
        stage('Test'){
            steps{
                script{
                    sh """
                        echo "This is Test stage"
                    """
                }
            }
        }
        stage('Deploy'){
            steps{
                script{
                    sh """
                        echo "This is deploy stage"
                    """
                }
            }
        }
    }
    post{
        always {
            echo 'I will always say hello again!'
        }
        failure {
            echo 'I will when pipeline is failed'
        }
        success {
            echo 'I will when pipeline is success'
        }
    }
}