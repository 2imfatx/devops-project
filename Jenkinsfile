pipeline {
    agent {
        docker {
            image 'gcc:latest'
        }
    }
    stages {
        stage('Build') {
            steps {
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
