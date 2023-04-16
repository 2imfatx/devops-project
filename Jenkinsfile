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
                sh 'sudo apt-get update'
            }
        }
        stage('Test'){
            steps{
                sh 'echo "Testing..."'
            }
        }
    }
}
