pipeline {
    agent {
        node{
         label 'docker-agent-alpine'
        }
      }
    stages {
        stage('Build') {
            steps {
                docker {
                    image 'gcc:latest'
                }
                sh 'echo "Building..."'
                sh 'apk update'
                sh 'apk add g++'
                sh 'g++ -o hello-world hello-world.cpp'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testing..."'
            }
        }
    }
}
