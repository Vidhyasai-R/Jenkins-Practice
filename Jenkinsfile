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
    stages{
        stage('Build'){
            steps{
                script{
                    sh """
                        echo "This is Build stage"
                        echo "Project: $PROJECT"
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
    post {
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