pipeline {
  agent {
    node{
     label 'docker-agent-alpine'
    }
  }
  options {
    // Run pipeline with elevated privileges
    docker { 
      image 'alpine'
      args '-u root'
    }
  }
  triggers {
    pollSCM '* * * * *'
  }
  stages{
    stage('Build'){
      steps{
       sh 'echo "Building..."'
       sh 'apk add --update g++'
       sh 'g++ -o hello-world hello-world.cpp'
      }
    }
    stage('Test'){
      steps{
       sh 'echo "Testing..."'
       sh './hello-world'
      }
    }
  }
}
