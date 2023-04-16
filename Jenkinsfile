pipeline {
    agent {
        node{
            label 'docker-agent-gcc'
        }
    }
    stages {
        stage('Build') {
            steps {
               sh 'echo test build'
            }
        }
        stage('Test') {
            steps {
                sh 'echo test'
            }
        }
    }
}
