pipeline {
    agent {
        label 'docker-agent-python'
    }
    stages{
        stage('Build'){
            steps{
                sh 'echo "Building..."'
                sh 'py'
            }
        }
        stage('Test'){
            steps{
                sh 'echo "Testing..."'
            }
        }
    }
}
