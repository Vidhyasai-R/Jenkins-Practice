pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                script{
                    sh """
                        echo 'This is Build stage'
                    """
                }
            }
        }
        stage('Test'){
            steps{
                script{
                    sh """
                        echo 'This is Test stage'
                    """
                }
            }
        }
    }
}