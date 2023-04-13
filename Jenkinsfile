pipeline {
  agent {
    node{
     label 'docker-agent-gcc'
    }
  }
  triggers {
    pollSCM '*/5 * * * *'
  }
  stages{
    stage('Build'){
      steps{
       sh 'echo "Building..."'
       sh 'g++ -o hello-world hello-world.cpp'
      }
    }
    stage('Test'){
      steps{
       sh 'echo "Testing..."'
       sh './hello-world'
       sh 'echo test'
      }
    }
  }
}
