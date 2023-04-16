pipeline {
    agent {
        docker {
            image 'alpine:latest'
            args '--user=root'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'apk add build-base'
                sh 'g++ -o my_app hello.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './my_app'
            }
        }
    }
}
