pipeline{
    agent {label 'AGENT-1'}
    stages{
        stage('Build'){
            steps{
                script{
                    sh """
                        echo "This is Build stage"
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
}