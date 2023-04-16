pipeline {
    agent {
        label 'docker-agent-alpine'
    }
    triggers {
        pollSCM '* * * * *'
    }
    stages{
        stage('Build'){
            steps{
                sh 'echo "Building..."'
            }
        }
        stage('Test'){
            steps{
                sh 'echo "Testing..."'
            }
        }
    }
}
