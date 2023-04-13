pipeline {
  agent {
    node{
     label 'docker-agent-alpine'
    }
  }
  triggers {
    pollSCM '*/5 * * * *'
  }
  stages{
    stage('Build'){
      steps{
       sh 'echo "Building..."'
       sh 'sudo -y apt install g++'
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
