pipeline {
  agent {
    node {
      label 'docker-agent-alpine'
    }
  }
  triggers {
    pollSCM '* * * * *'
  }
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
        sh 'apk add --update g++'
        sh 'g++ -o hello-world hello-world.cpp'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing...'
        sh './hello-world'
      }
    }
  }
}
