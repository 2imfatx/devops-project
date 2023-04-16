pipeline {
    agent {
        node{
            label 'docker-agent-alpine'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'apk add build-base'
                sh 'sudo g++ -o my_app hello.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './my_app'
            }
        }
    }
}
