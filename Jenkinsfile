pipeline {
    agent {
        docker {
            image 'gcc'
            args '-v /var/run/docker.sock:/var/run/docker.sock'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o myapp myapp.cpp'
            }
        }
    }
}
