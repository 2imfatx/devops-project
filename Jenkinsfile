pipeline {
    agent {
        label 'docker-agent-python'
    }
    triggers {
        pollSCM '* * * * *'
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
